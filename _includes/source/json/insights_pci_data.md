{% highlight json %}
{
    "bundle_id": "abcde12345",
    "created": "2015-05-16T20:39:37.507Z",
    "id": "54321edcba",
    "name": "pci_data",
    "status": "ready",
    "track_data": [
        {
            "track_id": "fff111",
            "track_label": "",
            "pci_data": [
                {
                    "start": 42.1,
                    "end": 53.07
                }, {
                    "start": 56.2,
                    "end": 58.3
                }, {
                    "start": 64.2,
                    "end": 67.95
                }
            ]
        }
    ],
    "updated": "2015-05-16T20:39:37.508Z",
    "_class": "PciDataInsight",
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