# Clarify's Documentation Pages

This is the repository for all the documentation for the Clarify.io API which is currently at docs.github.io.

While this is the current version of our documentation, it was not the first. Check out [An Evolution on Documentation](http://clarify.io/blog/an-evolution-in-documentation/) to understand some of our how and why we got here.

## Adding a Quickstart

1. Create a file in the _quickstarts folder for the Quickstart you plan to write
  * Make sure to set the 'languages' array, that determines which tabs appear for the code samples
  * Make sure to set the 'navtitle' and 'order' values, those determine the link and its order in the sidebar navigation
1. Include the sections which you need from the _includes/sections folder
1. Anytime you want to include a code sample, create a variable called 'tabs' with the name of your samples and include /structural/tabs.html
  * Whatever string you use for the 'tabs' variable should be the name of your code samples.
    * For example, if 'tabs' equals 'monkey' then your PHP sample would be in _includes/source/php/monkey.md while the curl example would be _includes/source/curl/monkey.md
  * Once you have all the samples you want in whatever language, simply add that language to the 'languages' array in the Quickstart front matter.
    * Make sure that you have **all** the samples for a given language before you turn it on. Otherwise the includes will fail and Jekyll won't update the pages.

## Todo list

* ~~Convert existing site~~
* ~~Set up basic template w/ header, footer, etc~~
* ~~Move all the code from Gists into the repo~~
* ~~Find a good syntax highlighter~~
* Add a directory of errors
* Add a directory of callback formats
* Convert the swagger iframe to actual docs
* Insights & Reports
  * Spoken Words Report
  * ~~Topics Insight (beta)~~
  * Closed Captioning (beta)
* Code samples
  * Implement PHP for everything
  * Implement Python for everything
  * Implement Java for everything
  * Implement Ruby for everything
  * Implement Node for everything
  * Implement C# for everything
  * ~~Rename includes to be easier to predict~~
  * ~~Add the bundle callback to the basic search quickstart~~
  * Replace the "processed" search results with the raw json
  * Add keyword processing to that quickstart
* Formatting
  * ~~Make it so that things outside paragraphs are formatted correctly~~
  * ~~Remove the paragraphs~~
  * Kill some of the stupid CSS
  * ~~Improve the formatting of inline code/words to stand out better~~
  * ~~Make sure links open in the right windows~~
  * ~~Simplify includes to minimize duplication~~
  * ~~Fix the header/footer margin around the code samples~~
  * ~~Expand the margin between the code samples and the next paragraph/text~~
  * ~~Convert back to the default syntax highlighting where possible~~
* Use front matter better
  * ~~Tag things that are in beta and invite-only~~
  * ~~Add quickstarts to sidebar via a collection~~
  * ~~Shift messages into a subfolder~~
* Move media list out of WordPress

## Contributing

If you want to run this locally yourself, check out Github's getting started documentation here: https://help.github.com/articles/using-jekyll-with-pages/

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request from github