{% highlight json %}
{
    "id": "fadbe23456",
    "bundle_id": "abcde12345",
    "name": "captions_r4",
    "status": "ready",
    "created": "2015-12-20T15:47:20.459Z",
    "updated": "2015-12-20T16:00:56.298Z",
    "track_data": [
        {}
    ],
    "_class": "CaptionsR4Insight",
    "_links": {
        "self": {
            "href": "/v1/bundles/abcde12345/insights/fadbe23456"
        },
        "curies": [
            {
                "href": "/docs/rels/{rel}",
                "name": "clarify",
                "templated": true
            },
            {
                "href": "/docs/insights/captions/{rel}",
                "name": "captions",
                "templated": true
            }
        ],
        "parent": {
            "href": "/v1/bundles/abcde12345/insights"
        },
        "clarify:bundle": {
            "href": "/v1/bundles/abcde12345"
        },
        "captions:vtt": [
            {
                "href": "/v1/bundles/abcde12345/insights/fadbe23456/_links?rel=captions%3Avtt&track_id=badee12345",
                "name": "badee12345"
            }
        ],
        "captions:srt": [
            {
                "href": "/v1/bundles/abcde12345/insights/fadbe23456/_links?rel=captions%3Asrt&track_id=badee12345",
                "name": "badee12345"
            }
        ]
    }
}
{% endhighlight %}