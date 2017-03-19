# Ember Routing Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Ember.js - Routing: Specifying a Route's Model](https://guides.emberjs.com/v2.11.0/routing/specifying-a-routes-model/)
-   [danwebb.net - It's About The Hashbangs](http://danwebb.net/2011/5/28/it-is-about-the-hashbangs)
-   [Ember.js - Configuring Ember.js: Specifying the URL Type](https://guides.emberjs.com/v2.11.0/configuring-ember/specifying-url-type/)
-   [Deploying Ember CLI apps to GitHub Pages](http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
Ember is able to load different view states by using dynamic segments when defining
routes for URLs. Ember takes the value of the dynamic piece of the route and then
passes it as a hash to the model .

In general, the route is passed through the router and then the route handler, which
is where a template and the model are loaded. Here, data can be persisted to the
server. The template will load the components (smaller pieces that make up
the entire template) and then they will access the data from the model.

sources:
https://guides.emberjs.com/v2.5.0/routing/specifying-a-routes-model/
https://guides.emberjs.com/v2.9.0/getting-started/core-concepts/
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs use the anchor of a URL (like www.google.com) and then an ending path
with a hash (#) at the end (like /#/books/old). The hash is supposed to keep
things in sync as the user moves around the site.
Source: https://guides.emberjs.com/v2.5.0/configuring-ember/specifying-url-type/

When deploying to gh-pages, it is important to reference image data using paths
WITHOUT the slash prefix. For example, an image could be referenced like:
url('images/new.jpg') - without the initial forward slash. The slash prefix
would imply that it is a full path on the HTTP server when it is not.
source: http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html

If you want to use the history API instead of the hash for location, you would
use /location instead of /#/location.
https://guides.emberjs.com/v2.5.0/configuring-ember/specifying-url-type/
```
