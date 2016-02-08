{% highlight json %}
{
    "bundle_id": "abcde12345",
    "name": "bundle name",
    "external_id": "external_123",
    "insight": "transcript_r9",
    "insight_id": "12345edcba",
    "updated": "2015-04-30T01:11:19.889Z",
    "_class": "InsightNotification",
    "_links": {
        "curies": [
                 {
                     "href": "/docs/rels/{rel}", "name": "clarify", "templated": true
                 },
                 {
                     "href": "/docs/insights/{rel}", "name": "insight", "templated": true
                 }
             ],
             "clarify:insights": {
                 "href": "/v1/bundles/abcde12345/insights"
             },
             "clarify:bundle": {
                 "href": "/v1/bundles/abcde12345"
             },
             "clarify:tracks": {
                 "href": "/v1/bundles/abcde12345/tracks"
             },
             "insight:transcript_r9": {
                 "href": "/v1/bundles/abcde12345/insights/12345edcba"
             }
    }
}
{% endhighlight %}