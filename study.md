# Ember Routing Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Ember.js - Routing: Specifying a Route's Model](https://guides.emberjs.com/v2.5.0/routing/specifying-a-routes-model/)
-   [danwebb.net - It's About The Hashbangs](http://danwebb.net/2011/5/28/it-is-about-the-hashbangs)
-   [Ember.js - Configuring Ember.js: Specifying the URL Type](https://guides.emberjs.com/v2.5.0/configuring-ember/specifying-url-type/)
-   [Deploying Ember CLI apps to GitHub Pages](http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
The URL is first processed by the router. The router activates the proper route,
or route handler, which access models. The data from the model then gets
passed from the route handler to a template which is what renders the view state.

```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs are URLs that have /#/ before the route name in the URL. They can be used
along with hashchange events to track the state of the app, as an alternative to
a browser's history API. If you want to use the history API, it needs to be supported
by the browser.

When you deploy an ember app to gh-pages, you should use a tool like ember-cli-github-pages.
You will have to build first with: ember build --environment production
and then move dist to gh-pages before pushing.

You should be aware that urls for resources like images are going to be
relative, so they should not start with a slash.
```
