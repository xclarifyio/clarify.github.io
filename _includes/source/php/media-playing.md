{% highlight php %}
<?php

require 'vendor/autoload.php';

$bundle = new Clarify\Bundle('my api key');
$items = $bundle->search($terms);

$search_terms = json_encode($items['search_terms']);
$item_results = json_encode($items['item_results']);

$audiokey = $items['_links']['items'][0]['href'];
$tracks = $bundle->tracks->load($audiokey)['tracks'];
$mediaUrl = $tracks[0]['media_url'];
{% endhighlight %}