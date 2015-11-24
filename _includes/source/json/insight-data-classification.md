{% highlight json %}
{
    "_class": "ClassificationInsight",
    "bundle_id": "abcde12345",
    "created": "2015-09-17T18:48:48.058Z",
    "id": "edcba56789",
    "name": "classification",
    "status": "ready",
    "updated": "2015-09-17T18:48:48.061Z",
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
            "href": "/v1/bundles/abcde12345/insights/edcba56789"
        }
    },
    "track_data": [
            {
                "acoustics": [],
                "spoken_languages": ["fr"]
            }
        ]
}
{% endhighlight %}