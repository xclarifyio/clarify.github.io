{% highlight bash %}
curl https://api.clarify.io/v1/search?query=dorothy \
    --header "Authorization: Bearer myapikey" | jq '.'
# The jq portion is optional and just used to pretty print the resulting json
{% endhighlight %}