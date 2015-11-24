{% highlight python %}
from clarify_python import clarify

client = clarify.Client('my api key')

client.create_bundle(name='Dorothy and the Wizard of Oz',
        media_url='http://media.clarify.io/audio/books/dorothyandthewizardinoz_01_baum_64kb.mp3')
{% endhighlight %}