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

A route often includes a model hook, which pulls in the necessary data for a
view-state. Ember loads that data and passes it to the template by way of the
controller. Routes can have "dynamic segments" (parameters, query strings)
that reference, for example, specific data ids or search terms. Ember parses
these segments and makes them available to the model hook within the route so
that the appropriate data can be loaded.

```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md

Hashbang URLs (domain.com/#!/content) don't send anything after the hash as
part of the HTTP request.

Using the `history` API requires that your server serve your Ember app from
each URL in the router.js file. (It sounds like this isn't possible with GH
Pages?)

Hash URLs (ember.app/#/content) rely on the `hashchange` event in the browser
(which is widely supported), but Dan Webb argues that this approach is bad—it
subverts HTTP status codes (which are good! and useful!) and means that
JavaScript is responsible for displaying errors, redirecting, etc.

GitHub pages requires that you set `ENV.locationType` to `hash` so that it can
properly handle all of the app's assets (images, etc.).

```
