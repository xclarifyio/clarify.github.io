{% highlight json %}
{
    "id": "98765abcde",
    "bundle_id": "abcde12345",
    "name": "transcript_r9",
    "status": "ready",
    "created": "2015-05-14T21:50:17.245Z",
    "updated": "2015-05-14T21:57:30.139Z",
    "data": {
        "transcript": {
            "meta": {
                "format": "clarify_transcript",
                "version": 1
            },
            "segments": [
                {
                    "speaker": "Speaker 1",
                    "terms": [
                        {
                            "term": "Thank"
                        },
                        {
                            "term": "you"
                        },
                        {
                            "term": "for"
                        },
                        {
                            "term": "calling"
                        },
                        {
                            "term": "clarify"
                        },
                        {
                            "term": ".",
                            "type": "mark"
                        }
                    ]
                },
                {
                    "speaker": "Speaker 2",
                    "terms": [
                        {
                            "term": "How"
                        },
                        {
                            "term": "are"
                        },
                        {
                            "term": "you"
                        },
                        {
                            "term": "?",
                            "type": "mark"
                        }
                    ]
                },
                {
                    "speaker": "Speaker 1",
                    "terms": [
                        {
                            "term": "Good"
                        },
                        {
                            "term": ".",
                            "type": "mark"
                        },
                        {
                            "term": "I'm"
                        },
                        {
                            "term": "well"
                        },
                        {
                            "term": ",",
                            "type": "mark"
                        },
                        {
                            "term": "thank"
                        },
                        {
                            "term": "you"
                        },
                        {
                            "term": ".",
                            "type": "mark"
                        }
                    ]
                }
            ],
            "speakers": [
                {
                    "id": "Speaker 1",
                    "label": "Agent"
                },
                {
                    "id": "Speaker 2",
                    "label": "Customer"
                }
            ]
        }
    },
    "_class": "TranscriptR9Insight",
    "_links": {
        "self": {
            "href": "/v1/bundles/89612c28760343e5898aa059f7980a7e/insights/11c472b8e6de4275a61509a2f7de134a"
        },
        "curies": [
        {
            "href": "/docs/rels/{rel}",
            "name": "clarify",
            "templated": true
        }
        ],
        "parent": {
            "href": "/v1/bundles/abcd1234/insights"
        },
        "clarify:bundle": {
            "href": "/v1/bundles/abcd1234"
        }
    }
}
{% endhighlight %}