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
Ember router maps the current URL to one or more route handlers. And route handler will load a model that is avaliable to the template and render a template for loading view-state.
After url come, the router layer will indicate specific route to reads the URL and uses the model hook, model layer will returns the ember data. After data finish loading, route will render the template.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URL: Uses URL anchor to load the starting state of an application and keep it in sync when a user navigates around the page;

When deploying to GH pages, don't prefix image paths with /, because it is a full path on the HTTP server;

You don't have to change anything to use the 'history' API instead of 'hash', because Ember defaults the router to use 'auto' which uses 'history' if supported by the user's browser.  Changes to this configuration can be made in 'config/environment.js' file.
```
