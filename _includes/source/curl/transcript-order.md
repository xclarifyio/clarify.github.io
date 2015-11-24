{% highlight bash %}
curl --data "insight=transcript_r9" https://api.clarify.io/v1/bundles/abcde12345/insights \
     --header "Authorization: Bearer myapikey" | jq '.'
# The jq portion is optional and just used to pretty print the resulting json
{% endhighlight %}