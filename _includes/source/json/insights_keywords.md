{% highlight json %}
{
    "bundle_id": "abcde12345",
    "created": "2015-05-16T20:39:37.507Z",
    "id": "54321edcba",
    "name": "spoken_keywords",
    "status": "ready",
    "track_data": [
        {
            "keywords": [
                {
                    "count": 11,
                    "term": "horse",
                    "weight": 0.917
                }, {
                    "count": 9,
                    "term": "uncle",
                    "weight": 0.75
                }, {
                    "count": 7,
                    "term": "dorothy",
                    "weight": 0.583
                }, {
                    "count": 5,
                    "term": "little",
                    "weight": 0.417
                }, {
                    "count": 4,
                    "term": "train",
                    "weight": 0.333
                }
            ]
        }
    ],
    "updated": "2015-05-16T20:39:37.508Z",
    "_class": "SpokenKeywordsInsight",
    "_links": {
        "clarify:bundle": {
            "href": "/v1/bundles/abcde12345"
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
        "self": {
            "href": "/v1/bundles/abcde12345/insights/54321edcba"
        }
    }
}
{% endhighlight %}