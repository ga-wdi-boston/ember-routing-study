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
The routing layer (router) maps URLs to routes. The router passes any relevant
params to the route handler for that route. The route handlers includes a method
called the model hook, which is fired (with params as an argument if necessary)
to retrieve the correct model from the data layer. The retrieved model is passed
to that route's template, which uses data from the model, along with any
necessary components, to render content for the UI. The content that is
subsequently displayed in the UI is considered the 'view-state' for that URL.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
A hash URL is the optional second half of a URL that comes after the '#' symbol.
This portion of the URL is not sent to the server and is used only for local
navigation.

When using GitHub Pages to deploy an Ember app, it is important to:
-  reference image paths differently from CSS vs templates
-  set `ENV.locationType` in `config/environment.js` to `'hash'`
-  build the project to `dist/`
-  copy `dist/` to the root, `git add` relevant files, commit and push

To use the `history` API instead of `hash` for `location`, `ENV.locationType`
must be set to `history`. Alternately, you can use `auto` (which is the default)
configuration. `auto` will use `history` if the browser supports it, and `hash`
if not.
```
