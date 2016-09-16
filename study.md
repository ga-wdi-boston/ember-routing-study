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
The router is responsible for loading the correct model, which will load the view state and the template will change the UI.

The router figures out what the user is looking at, and if they select something, the router maps the current URL to a route handler that will perform the correct action.

The router can load a model, which represents the underlying data that is shown to the user. The models can store the data to a database if the user leaves the page, or it can even store to the user's own database.  The data is stored as JSON.

Templates are used as the user interface.

Components consist of templates whose purpose is to be reused in multiple view states to eliminate repetitition in the other model-specific templates.

Controllers behave like components.

```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs turn everything after the hash in the URL into an identifier.
Full path names must be written when deploying ember to gh-pages and the config/environment.js must have a baseURL with a path '/project-name'.  The history API requires all routes to be represented in the back end.
```
