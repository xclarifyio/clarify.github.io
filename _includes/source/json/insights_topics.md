{% highlight json %}
{
    "id": "34567abcde",
    "bundle_id": "abcde12345",
    "name": "spoken_topics",
    "status": "ready",
    "created": "2015-11-23T22:52:37.450Z",
    "updated": "2015-11-23T22:52:37.454Z",
    "track_data": [
        {
            "topics": [
                {
                    "categories": [
                        {
                            "path": [
                                {
                                    "name": "Sociology"
                                },
                                {
                                    "name": "Interpersonal Relationships"
                                }
                            ]
                        }
                    ],
                    "terms": [
                        {
                            "term": "life"
                        },
                        {
                            "term": "time"
                        },
                        {
                            "term": "born"
                        },
                        {
                            "term": "family"
                        },
                        {
                            "term": "father"
                        },
                        {
                            "term": "death"
                        },
                        {
                            "term": "year"
                        },
                        {
                            "term": "son"
                        },
                        {
                            "term": "man"
                        },
                        {
                            "term": "wrote"
                        },
                        {
                            "term": "mother"
                        },
                        {
                            "term": "began"
                        },
                        {
                            "term": "wife"
                        },
                        {
                            "term": "made"
                        },
                        {
                            "term": "named"
                        },
                        {
                            "term": "home"
                        },
                        {
                            "term": "young"
                        }
                    ]
                }
            ]
        }
    ],
    "_class": "SpokenTopicsInsight",
    "_links": {
        "self": {
            "href": "/v1/bundles/abcde12345/insights/34567abcde"
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