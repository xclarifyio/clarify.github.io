---
layout: default
title: Error And Warning Codes
---

# Common Error And Warning Codes

- - -

### HTTP Response Codes

* **400 Bad Request** - Your request failed. This is usually due to a missing/wrong parameter.
* **401 Unauthorized** - You did not successfully authenticate. Check [your API Key](https://developer.clarify.io/apps/list/) and try again.
* **404 Not Found** - You requested an endpoint that doesn't exist.
* **409 Conflict** - You attempted to update a resource which has been changed since your last request. Re-request the resource and apply your changes again.

We use a few other HTTP Response Codes which you can [read about on our blog](http://clarify.io/blog/http-response-codes-and-you/).

### Media Processing Codes

After you create a bundle, we'll attempt to retrieve and analyze your media and each track will have it's <code>media_code</code> and a <code>media_message</code> set.

* **1000 OK** - It worked! Time to celebrate!
* **1100 File error** - The file was empty.
* **1101 File too large** - The file was over 8 gigabytes.
* **1200 Malformed file** - The file structure was not a properly formatted supported codec.
* **1201 Unsupported codec** - The file is not one of [our supported codecs](http://clarify.io/blog/audio-and-video-formats-for-the-clarify-api/).
* **1203 Non audio or video codec** - The file was not a media type that contains audio or video.
* **1204 No audio** - The file did not contain any audio signal to process.
* **1301 Duration too short** - The media was less than 1 second long.
* **1302 Duration too long** - The media was over 120 minutes long.
