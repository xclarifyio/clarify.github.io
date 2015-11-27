---
layout: default
title: Libraries and SDKs
---

# Helper Libraries and SDKs

- - -

Use one of our helper libraries to use Clarify in your language of choice:

* <a href="https://github.com/Clarify/clarify-php" onclick="_gaq.push(['_trackEvent', 'outbound-article', 'https://github.com/Clarify/clarify-php', 'clarify-php']);" title="Clarify PHP Library">clarify-php</a> &mdash; Requires PHP 5.3+, installed via Composer
* <a href="https://github.com/Clarify/clarify_python_2" onclick="_gaq.push(['_trackEvent', 'outbound-article', 'https://github.com/Clarify/clarify_python_2', 'clarify-python 2']);" title="Clarify Python Library">clarify-python 2</a> &mdash; Requires Python 2.x, installed via Pip
* <a href="https://github.com/Clarify/clarify_python" onclick="_gaq.push(['_trackEvent', 'outbound-article', 'https://github.com/Clarify/clarify_python', 'clarify-python 3']);" title="Clarify Python Library">clarify-python 3</a> &mdash; Requires Python 3.x, installed via Pip
* <a href="https://github.com/Clarify/clarify-java" onclick="_gaq.push(['_trackEvent', 'outbound-article', 'https://github.com/Clarify/clarify-java', 'clarify-java']);" title="Clarify Java Library">clarify-java</a> &mdash; Requires Java 1.6+, installed via Maven
* <a href="https://github.com/Clarify/clarify-ruby" onclick="_gaq.push(['_trackEvent', 'outbound-article', 'https://github.com/Clarify/clarify-ruby', 'clarify-ruby']);" >clarify-ruby</a> &mdash; Requires Ruby 2.0+, installed via Ruby gems
* <a href="https://github.com/Clarify/clarify-csharp" onclick="_gaq.push(['_trackEvent', 'outbound-article', 'https://github.com/Clarify/clarify-csharp', 'clarify-csharp']);" title="Clarify C-Sharp Library">clarify-csharp</a> &mdash; Requires .Net 4.x, installed via Nuget
* <a href="https://github.com/Clarify/clarify-curl" onclick="_gaq.push(['_trackEvent', 'outbound-article', 'https://github.com/Clarify/clarify-curl', 'curl examples']);" >curl examples</a>

It's dangerous to go alone. The helper libraries handle authentication, the HTTP aspects, and even wrap commonly needed functionality in language-specific constructs. You can focus on your app.

We provide helper libraries in the languages we use on a regular basis. While we're open to creating and adding more, we want to know which ones you care about. <em><a href="mailto:support@clarify.io">Email us to tell us what you need!</a></em>

- - -

### SDK Writing Guide

Our goal is to provide helper libraries in the most relevant languages as quickly as possible but sometimes our roadmap doesn't match your timeline. Fear not! Here are some tips and information to get you started.

In terms of helper library design, we see four layers:

* Authentication/Connectivity
* Response/Result handling
* Domain Models
* Framework-specific opinions

In our language libraries, we will only deal with the first two layers. The final two layers should be handled by framework/domain-specific libraries built on top of our libraries. If you do build something, <a href="mailto:support@clarify.io">let us know</a> so we can give show off your efforts on this page!

Here are some general guidelines to get you started:

* MUST be idiomatic with the language in which it is written. For example, a C# library will use data structures and patterns common to that platform.
* MUST follow the commonly accepted coding standards of the language in which it is written.
* MUST handle authentication, connectivity, and responses in a consistent manner.
* SHOULD have behavior tests to demonstrate it works as described.
* SHOULD pass along errors as appropriate for the language.
* MUST NOT hide errors from end users.
* MAY encapsulate language/framework-specific opinions, data structures, and processes.