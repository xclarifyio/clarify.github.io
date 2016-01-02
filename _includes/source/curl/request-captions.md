{% highlight bash %}
curl https://api.clarify.io/v1/bundles/abcde12345/insights/fadbe23456 \
    --header "Authorization: Bearer myapikey"  | jq '.'
# The jq portion is optional and just used to pretty print the resulting json
{% endhighlight %}