{% highlight json %}
{
    "bundle_id":"abcde12345",
    "updated":"2014-08-25T22:12:39.574Z",
    "bundle_processing_cost":0.1,
    "name":"Harvard Sentences 1",
    "external_id":"my_id_123",
    "_class":"BundleNotification",
    "_links":{
        "curies":[
            {
                "href":"/docs/rels/{rel}", "name":"clarify", "templated":true
            }
        ],
        "clarify:bundle":{
            "href":"/v1/bundles/abcde12345"
        },
        "clarify:tracks":{
            "href":"/v1/bundles/abcde12345/tracks"
        },
        "clarify:metadata":{
            "href":"/v1/bundles/abcde12345/metadata"
        },
        "clarify:insights":{
            "href":"/v1/bundles/abcde12345/insights"
        }
    }
}
{% endhighlight %}