# Ember Routing Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Watching

-   [CascadiaJS 2013 - Tom Dale - Stop Breaking the Web - YouTube](https://www.youtube.com/watch?v=BQ6at0addi4)

## Required Readings

-   [Ember.js - Routing: Specifying a Route's Model](https://guides.emberjs.com/v2.4.0/routing/specifying-a-routes-model/)
-   [danwebb.net - It's About The Hashbangs](http://danwebb.net/2011/5/28/it-is-about-the-hashbangs)
-   [Ember.js - Configuring Ember.js: Specifying the URL Type](https://guides.emberjs.com/v2.4.0/configuring-ember/specifying-url-type/)
-   [Deploying Ember CLI apps to GitHub Pages](http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

## Ember and URLs

In your own words, how Ember "stops breaking the web".

When we made single-page-apps without Ember, with just jquery and javascript, we broke the page each time we refreshed or hit the back button.  However in Ember-built apps, different parts of the content have unique routes and URLs. This provides a better user experience, so that users can bookmark and share the URLs.

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

In the router layer, Ember uses the URL to route to the appropriate model and load a specific template.

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

Ember apps require running an Ember server to respond to requests. If you simply deploy to a static server like gh-pages as is, your website will not work to get the server requests. You can circumvent this with hash urls, which anchor the urls to load the starting state of the app and keep it in sync as new content maybe be loaded as users navigate the page.

If you want to use history API instead of hash, you can’t deploy on Github.
