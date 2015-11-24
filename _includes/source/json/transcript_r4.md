{% highlight json %}
{
    "id": "98765abcde",
    "bundle_id": "abcde12345",
    "name": "transcript_r4",
    "status": "ready",
    "created": "2015-06-27T16:18:05.573Z",
    "updated": "2015-06-27T16:21:08.917Z",
    "track_data": [
    {
        "transcript":
        {
            "meta": {
                "format": "clarify_transcript",
                "version": 1.0
            },
            "segments": [
                {
                    "language": "en-US",
                    "start": 0.94,
                    "dur": 3.45,
                    "terms": [
                        {
                            "dur": 0.28,
                            "term": "Thanks",
                            "start": 0.94
                        }, {
                            "dur": 0.12,
                            "term": "for",
                            "start": 1.22
                        }, {
                            "dur": 0.32,
                            "term": "calling",
                            "start": 1.37
                        }, {
                            "dur": 0.14,
                            "term": "the",
                            "start": 1.77
                        }, {
                            "dur": 0.45,
                            "term": "clarify",
                            "start": 1.91
                        }, {
                            "dur": 0.95,
                            "term": "API",
                            "start": 2.36
                        }, {
                            "dur": 0.32,
                            "term": "example",
                            "start": 3.53
                        }, {
                            "dur": 0.36,
                            "term": "desk",
                            "start": 4.03
                        }, {
                            "start": 4.39,
                            "term": ".",
                            "dur": 0,
                            "type": "mark"
                        }
                    ]
                }, {
                    "language": "en-US",
                    "start": 6.31,
                    "dur": 2.42,
                    "terms": [
                        {
                            "dur": 0.22,
                            "term": "We",
                            "start": 6.31
                        }, {
                            "dur": 0.11,
                            "term": "are",
                            "start": 7.13
                        }, {
                            "dur": 0.19,
                            "term": "here",
                            "start": 7.52
                        }, {
                            "dur": 0.15,
                            "term": "to",
                            "start": 8.26
                        }, {
                            "dur": 0.09,
                            "term": "help",
                            "start": 8.41
                        }, {
                            "dur": 0.18,
                            "term": "you",
                            "start": 8.55
                        }, {
                            "start": 8.73,
                            "term": ".",
                            "dur": 0,
                            "type": "mark"
                        }
                    ]
                }
            ]
        }
    }
    "_class": "TranscriptR4Insight",
    "_links": {
        "self": {
            "href": "/v1/bundles/abcde12345/insights/54321edcba"
        },
        "curies": [
            {
                "href": "/docs/rels/{rel}",
                "name": "clarify",
                "templated": true
            }
        ],
        "parent": {
            "href": "/v1/bundles/abcde12345/insights"
        },
        "clarify:bundle": {
            "href": "/v1/bundles/abcde12345"
        }
    }
}
{% endhighlight %}