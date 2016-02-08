{% highlight json %}
{
    "bundle_id":"abcde12345",
    "track_id":"54321edcba",
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
            "href":"/v1/bundles/abcde12345/tracks/54321edcba"
        },
        "clarify:tracks":{
            "href":"/v1/bundles/abcde12345/tracks"
        },
        "clarify:bundle":{
            "href":"/v1/bundles/abcde12345"
        }
    },
    "_embedded":{
        "clarify:track":{
            "id": "54321edcba",
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
                    "href":"/v1/bundles/abcde12345/tracks/54321edcba"
                },
                "parent":{
                    "href":"/v1/bundles/abcde12345/tracks"
                },
                "clarify:bundle":{
                    "href":"/v1/bundles/abcde12345"
                }
            }
        }
    }
}
{% endhighlight %}