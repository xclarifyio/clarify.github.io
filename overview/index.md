---
layout: default
title: Overview
---

# Clarify API Overview

- - -

Clarify provides a RESTful API to extract knowledge from audio and video content. API calls use the standard HTTP methods (GET, POST, PUT, DELETE) to perform operations on resources. Responses are in the hypermedia JSON format <a target="_blank" href="https://github.com/mikekelly/hal_specification/blob/master/hal_specification.md">HAL</a>. If you're not familiar with HAL, it's basically the JSON you already know and love plus a couple of extra concepts: *links* to related resources and the *ability to embed related resources* in the response. By using this format, you can build smarter applications and use generic API tools like the <a href="https://api.clarify.io/hal-browser/#/v1" target="_blank">HAL browser</a>, a UI for browsing your data and trying API calls.

## Core Concepts

The Clarify API defines the following models:

* **Bundle** is a set of media files and metadata which represent a single item.

* **Metadata** is arbitrary JSON data that is associated with a bundle. Metadata are arbitrary but can be used to search and filter results. For example, a video may include metadata including the title, producer, description, date, and location. A phone recording may contain two media files (one for each speaker on the call) and metadata including the phone numbers, names, and date of the call.

* **Tracks** define the media files in a bundle. A bundle can contain one or more tracks, as well as other information such as the audio channel to use, the language of the track, etc. Tracks are played simultaneously - *like left and right channels* - as opposed to sequential segments.

* **Insight** is information extracted from media such as language, keywords, topics etc.

## Requests and Responses

### Authentication

All requests are performed via HTTPS and use a bearer token in an ``Authorization: Bearer`` header for each request.

### Date Format

All dates are represented as JSON strings in the <a href="http://www.w3.org/TR/NOTE-datetime" target="_blank">ISO 8601</a> format in UTC (timezone Z) with millisecond precision. For example, "2014-02-25T14:23:45.000Z".

### Language Codes

Languages are represented as a language and region pair as defined in <a href="http://tools.ietf.org/html/rfc5646" target="_blank">RFC 5646</a>. For example "en-US".

### Request Format

* For GET and DELETE requests, use standard query string parameters.
* For POST and PUT requests, data is sent in the document body. The supported content types are ``application/x-www-form-urlencoded`` and ``multipart/form-data`` for form parameters and ``application/json`` for JSON parameters.

### Response Format

* Responses will always be HAL JSON format with one extra property *_class*, which defines the response class and can be used by client apps to aid with response processing. Currently supported classes are Bundle, Tracks, Metadata, Ref, Collection, and Error.
* The response Content-Type is ``application/hal+json``.
* Responses will use standard HTTP status codes. Successful responses will return a 2xx code while failed responses will return a 4xx code appropriate for the situation.

### Error Format

Errors will use the most appropriate HTTP status code and contain a HAL response in the following form:

    {
        "status": "Bad Request",
        "message": "the value of bundle_id must be a valid GUID",
        "code": 400,
        "errors": [{
           "field": "bundle_id",
           "message": "the value of bundle_id must be a valid GUID"
        }],
        "_class": "Error",
        "_links": {}
    }

More information on error codes can be found <a href="/errors/">here.</a>

### Notifications

Notifications are webhooks: URL endpoints that are automatically requested as work is completed by the Clarify API. To receive these notifications, include a **notify_url** for your bundle at creation. All notifications will be POSTed there.

There are three types of notifications: **TrackNotification**, **BundleNotification**, and **InsightNotification**.

#### Track Notifications

Track Notifications will inform you if the file was retrieved successfully or not. An example notification:

{% include /source/json/notification_track.md %}

#### Bundle Notifications

Bundle Notifications will inform you the total cost of the media processing. An example notification:

{% include /source/json/notification_bundle.md %}

#### InsightNotifications

Insight Notifications are sent when a specific insight is complete. The **insight** property contains the name and data of the insight and can be fetched by a GET request on the corresponding link relation called ``insight:insight_name``.  An example notification:

{% include /source/json/notification_insight.md %}

<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/8.6/highlight.min.js"></script>
<link rel="stylesheet" href="/assets/css/zenburn.css">
<script>hljs.initHighlightingOnLoad();</script>