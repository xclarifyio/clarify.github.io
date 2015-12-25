{% highlight bash %}
curl --data "media_url=http://media.clarify.io/video/presentations/SirKenRobinson-TED2006-How-Schools-Kill-Creativity.mp4" \
     --data "notify_url=http://example.org/sample-receiver" \
     --data "name=Sir Ken Robinson – TED 2006" https://api.clarify.io/v1/bundles \
     --X POST --header "Authorization: Bearer myapikey" | jq '.'
# The jq portion is optional and just used to pretty print the resulting json
{% endhighlight %}