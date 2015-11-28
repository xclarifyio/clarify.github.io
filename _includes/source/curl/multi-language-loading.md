{% highlight bash %}
curl --data "media_url=http://media.clarify.io.s3.amazonaws.com/video/speeches/je-vous-ai-compris-1958-06-04.mp4" \
     --data "notify_url=http://example.org/sample-receiver" \
     --data "name=Je Vous ai Compris" https://api.clarify.io/v1/bundles \
     --X POST --header "Authorization: Bearer myapikey" | jq '.'
# The jq portion is optional and just used to pretty print the resulting json
{% endhighlight %}