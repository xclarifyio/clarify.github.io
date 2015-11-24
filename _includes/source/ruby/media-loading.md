{% highlight ruby %}
require 'clarify'
require 'pp'

# This assumes that you set up your key in the environment using: export CLARIFY_API_KEY=myapikey
clarify = Clarify::Client.new(api_key: ENV['CLARIFY_API_KEY'])

created_bundle = clarify.bundles.create!(
    name: 'Dorothy and the Wizard of Oz',
    media_url: 'http://media.clarify.io/audio/books/dorothyandthewizardinoz_01_baum_64kb.mp3'
)

pp created_bundle
{% endhighlight %}