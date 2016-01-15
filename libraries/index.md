---
layout: default
title: Libraries and SDKs
---

# Helper Libraries and SDKs

- - -

Use one of our helper libraries to use Clarify in your language of choice:

* [clarify-php](https://github.com/Clarify/clarify-php) &mdash; Requires PHP 5.5+, installed via Composer
* [clarify-python 2](https://github.com/Clarify/clarify_python_2) &mdash; Requires Python 2.x, installed via Pip
* [clarify-python 3](https://github.com/Clarify/clarify_python) &mdash; Requires Python 3.x, installed via Pip
* [clarify-java](https://github.com/Clarify/clarify-java) &mdash; Requires Java 1.6+, installed via Maven
* [clarify-ruby](https://github.com/Clarify/clarify-ruby) &mdash; Requires Ruby 2.0+, installed via Ruby gems
* [clarify-csharp](https://github.com/Clarify/clarify-csharp) &mdash; Requires .Net 4.x, installed via Nuget
* [curl examples](https://github.com/Clarify/clarify.github.io/tree/master/_includes/source/curl)

It's dangerous to go alone. The helper libraries handle authentication, the HTTP aspects, and even wrap commonly needed functionality in language-specific constructs. You can focus on your app.

We provide helper libraries in the languages we use on a regular basis. While we're open to creating and adding more, we want to know which ones you care about. <em><a href="mailto:support@clarify.io">Email us to tell us what you need!</a></em>

Dive into <a href="/quickstarts/">our Quickstarts</a> to explore what is possible with the libraries.

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