{% highlight json %}
{
    "bundle_id": "abcde12345",
    "created": "2015-05-16T20:39:37.507Z",
    "id": "54321edcba",
    "name": "classification",
    "status": "ready",
    "track_data": [
        {
            "track_id": "fff111",
            "track_label": "",
            "spoken_languages": [
	        "en-US"
            ],
            "acoustics": [
	        "telephone"
            ]
        }
    ],
    "updated": "2015-05-16T20:39:37.508Z",
    "_class": "ClassificationInsight",
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