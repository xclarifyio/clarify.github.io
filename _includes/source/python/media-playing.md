{% highlight python %}
from clarify_python import clarify
import json

clarify.set_key('my api key')

result = clarify.search(query='dorothy')
search_terms = json.dumps(result['search_terms'])
item_results = json.dumps(result['item_results'])

bundleref = result['_links']['items'][0]['href']
bundle = clarify.get_bundle(bundleref)
tracksref = bundle['_links']['o3v:tracks']['href']
tracks = clarify.get_track_list(tracksref)['tracks']
mediaURL = tracks[0]['media_url']
{% endhighlight %}