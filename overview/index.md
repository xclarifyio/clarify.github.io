---
layout: default
title: Overview
---

# Clarify API Overview

- - -

Clarify provides a RESTful API to extract knowledge from audio and video content. API calls use the standard HTTP methods (GET, POST, PUT, DELETE) to perform operations on resource URLs. Responses are in the hypermedia JSON format <a target="_blank" href="https://github.com/mikekelly/hal_specification/blob/master/hal_specification.md">HAL</a>. If you're not familiar with HAL, it's basically the JSON you already know and love plus a couple of extra concepts: links to related resources and the ability to embed related resources in the response document. By using this format, the Clarify API allows you build smarter applications and use generic API tools like the <a href="https://api.clarify.io/hal-browser/#/v1" target="_blank">HAL browser</a>, a UI for browsing your data and trying API calls.

### Concepts

The Clarify API defines the following models:

* **Bundle** is a set of media and metadata which conceptually represent a single unit. For example, a video bundle may contain the video media and metadata listing the title, producer, description, date, and location. A phone recording bundle may contain two media files (one for each speaker on the call) and metadata listing the phone numbers, names, and date and time of the call.

* **Tracks** define the media in a bundle. A bundle can contain one or more tracks, each one specifying a media file, as well as other information such as the audio channel to use, the language of the track, etc.

* **Metadata** is arbitrary JSON data that is associated with a bundle. Metadata fields can be defined and contain whatever you would like to be able to search on and retrieve.

* **Insight** is information extracted from media such as spoken words, language, keywords, topics etc.


### Requests and Responses

#### Authentication

API users are provided with a bearer token which is used in an Authorization: Bearer header for each request (OAuth 2.0). For security, all requests are via HTTPS.

#### Date Format

Throughout the API, dates are represented as JSON strings in the <a href="http://www.w3.org/TR/NOTE-datetime" target="_blank">ISO 8601</a> format in UTC (timezone Z) with millisecond precision. For example, "2014-02-25T14:23:45.000Z".

#### Language Codes

Languages are specified as string codes representing a language and region pair as defined in <a href="http://tools.ietf.org/html/rfc5646" target="_blank">RFC 5646</a>. For example "en-US".

#### Request Format

Requests are HTTPS requests. For GET requests, use standard query string parameters. For POST and PUT requests, data is sent in the document body. The supported content types are application/x-www-form-urlencoded and multipart/form-data for form parameters and application/json for JSON data parameters.

#### Response Format

Responses will always be HAL JSON format with one extra property *_class*, which defines the response class and can be used by client apps to aid with response processing. Currently supported classes are Bundle, Tracks, Metadata, Ref, Collection, and Error. The response Content-Type is application/hal+json.

Responses will return the appropriate HTTP status code. Success responses may return a 200, 201, 202, or 204, depending on the context, so clients may wish to simply check for any 200-level response code to a determine successful request.

#### Error Format

Error responses will have the HTTP error code set and contain a HAL error response in the following form:

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

Notifications are webhooks; URL endpoints that are automatically hit when events occur within the Clarify API. Each bundle can specify an optional **notify_url** that is the URL used for all notifications for that bundle. The **notify_url** must be a publicly accessible url (http or https) on your server to which notifications for the bundle will be POSTed. For security, you may want to generate long URLs for this purpose.

For notifcations the POST body is a HAL JSON message containing the bundle_id, bundle name, and external_id if they have been set, as well as other data and standard Clarify link relations.

There are three types of notifications: TrackNotification, BundleNotification, InsightNotification.

#### **Track Notifications**

Track Notifications are sent when the status of a track in the bundle changes to an end state, either ready or error. Handling Track Notifications will allow you to know if a media fetch or media format error has occurred.

Example Track Notification POST body sent to a notify_url:

     {
         "bundle_id":"56b384d9749e4671960245a636701434",
         "track_id":"fef68854fe6e4e92aa1aa6ee2ab3cb99",
         "updated":"2014-08-25T22:12:39.574Z",
         "name":"Harvard Sentences 1",
         "external_id":"my_id_123",
         "_class":"TrackNotification",
         "_links":{
             "curies":[
                 {
                     "href":"/docs/rels/{rel}", "name":"clarify", "templated":true
                 }
             ],
             "clarify:track":{
                 "href":"/v1/bundles/56b384d9749e4671960245a636701434/tracks/fef68854fe6e4e92aa1aa6ee2ab3cb99"
             },
             "clarify:tracks":{
                 "href":"/v1/bundles/56b384d9749e4671960245a636701434/tracks"
             },
             "clarify:bundle":{
                 "href":"/v1/bundles/56b384d9749e4671960245a636701434"
             }
         },
         "_embedded":{
             "clarify:track":{
                 "id": "fef68854fe6e4e92aa1aa6ee2ab3cb99",
                 "track": 0,
                 "label": "",
                 "media_url": "http://media.clarify.io/audio/samples/harvard-sentences-1.wav",
                 "audio_channel": "",
                 "audio_language": "",
                 "created": "2014-08-25T19:54:26.123Z",
                 "updated": "2014-08-25T19:54:26.552Z",
                 "status": "ready",
                 "mime_type": "audio/x-wav",
                 "media_size": 1030810,
                 "duration": 64.422875,
                 "fetch_response_code": -1,
                 "fetch_response_message": "",
                 "media_code": -1,
                 "media_message": "",
                 "_class":"Track",
                 "_links":{
                     "self":{
                         "href":"/v1/bundles/56b384d9749e4671960245a636701434/tracks/fef68854fe6e4e92aa1aa6ee2ab3cb99"
                     },
                     "parent":{
                         "href":"/v1/bundles/56b384d9749e4671960245a636701434/tracks"
                     },
                     "clarify:bundle":{
                         "href":"/v1/bundles/56b384d9749e4671960245a636701434"
                     }
                 }
             }
         }
     }


#### **Bundle Notifications**

Bundle Notifications are sent when media processing has completed on a bundle and they will allow you to know the cost of the media processing.

Example Bundle Notification POST body sent to a notify_url:

    {
        "bundle_id":"56b384d9749e4671960245a636701434",
        "updated":"2014-08-25T22:12:39.574Z",
        "bundle_processing_cost":0.1,
        "name":"Harvard Sentences 1",
        "external_id":"my_id_123",
        "_class":"BundleNotification",
        "_links":{
            "curies":[
                {
                    "href":"/docs/rels/{rel}", "name":"clarify", "templated":true
                }
            ],
            "clarify:bundle":{
                "href":"/v1/bundles/56b384d9749e4671960245a636701434"
            },
            "clarify:tracks":{
                "href":"/v1/bundles/56b384d9749e4671960245a636701434/tracks"
            },
            "clarify:metadata":{
                "href":"/v1/bundles/56b384d9749e4671960245a636701434/metadata"
            },
            "clarify:insights":{
                "href":"/v1/bundles/56b384d9749e4671960245a636701434/insights"
            }
        }
    }


#### **InsightNotifications**

InsightNotifications are sent when an insight has finished running for a bundle and the data and be retrieved. The **insight** property contains the name of the insight and data for the insight can be fetched by doing a GET request on the corresponding link relation **insight:_insight_name_**.

Example Insight Notification POST body sent to a notify_url:

    {
        "bundle_id": "56b384d9749e4671960245a636701434",
        "name": "bundle name",
        "external_id": "external_123",
        "insight": "transcript_r9",
        "insight_id": "cba6d1fd1ca3426db41678887ac240b6",
        "updated": "2015-04-30T01:11:19.889Z",
        "_class": "InsightNotification",
        "_links": {
            "curies": [
                {
                    "href": "/docs/rels/{rel}", "name": "clarify", "templated": true
                },
                {
                    "href": "/docs/insights/{rel}", "name": "insight", "templated": true
                }
            ],
            "clarify:insights": {
                "href": "/v1/bundles/56b384d9749e4671960245a636701434/insights"
            },
            "clarify:bundle": {
                "href": "/v1/bundles/56b384d9749e4671960245a636701434"
            },
            "clarify:tracks": {
                "href": "/v1/bundles/56b384d9749e4671960245a636701434/tracks"
            },
            "insight:transcript_r9": {
                "href": "/v1/bundles/56b384d9749e4671960245a636701434/insights/cba6d1fd1ca3426db41678887ac240b6"
            }
        }
    }

