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

After you create a bundle, we'll attempt to retrieve your media and each track will get a <code>media_code</code> and a <code>media_message</code>.

* **1000 OK** - It worked! Time to celebrate!
* **1100 file_error** -
* **1101 file_too_large** -
* **1200 malformed_file** - The file structure did not match media codec stated.
* **1201 unsupported_codec** - The file is not one of [our supported codecs](http://clarify.io/blog/audio-and-video-formats-for-the-clarify-api/).
* **1203 non_audio_or_video_codec** - The file was not a media type we process.
* **1204 no_audio** - The file did not contain any speech to process.
* **1301 duration_too_short** -
* **1302 duration_too_long** -