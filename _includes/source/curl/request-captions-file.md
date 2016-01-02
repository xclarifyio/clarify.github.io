{% highlight bash %}
curl https://api.clarify.io/v1/bundles/abcde12345/insights/fadbe23456/_links?rel=captions%3Asrt&track_id=badee12345 \
    --header "Authorization: Bearer myapikey"  | jq '.'
# The jq portion is optional and just used to pretty print the resulting json
{% endhighlight %}