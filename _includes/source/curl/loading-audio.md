{% highlight bash %}
curl --data "media_url=http://media.clarify.io/audio/books/dorothyandthewizardinoz_01_baum_64kb.mp3" \
     --data "notify_url=http://example.org/sample-receiver" \
     --data "name=Dorothy and the Wizard of Oz" https://api.clarify.io/v1/bundles \
     --X POST --header "Authorization: Bearer myapikey" | jq '.'
# The jq portion is optional and just used to pretty print the resulting json
{% endhighlight %}