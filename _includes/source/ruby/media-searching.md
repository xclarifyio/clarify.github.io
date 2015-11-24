{% highlight ruby %}
require 'clarify'

clarify = Clarify::Client.new(api_key: 'docs-api-key')

results = clarify.bundles.search('dorothy')

results.each do |bundle_results, bundle_url|
    # Fetch the bundle:
    bundle = clarify.get(bundle_url)

    puts "#{bundle.name} - #{bundle_url}"
    bundle_results['term_results'].each do |term_result|
        term_result['matches'].each do |match|
            type = match['type']
            match['hits'].each do |hit|
                puts "\tmatched #{type} content at #{hit['start']} to #{hit['end']}"
            end
        end
    end
end
{% endhighlight %}