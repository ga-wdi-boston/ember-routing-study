# Ember Routing Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Ember.js - Routing: Specifying a Route's Model](https://guides.emberjs.com/v2.4.0/routing/specifying-a-routes-model/)
-   [danwebb.net - It's About The Hashbangs](http://danwebb.net/2011/5/28/it-is-about-the-hashbangs)
-   [Ember.js - Configuring Ember.js: Specifying the URL Type](https://guides.emberjs.com/v2.4.0/configuring-ember/specifying-url-type/)
-   [Deploying Ember CLI apps to GitHub Pages](http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
The router calls up a route in the app/routes folder. In the specified app/routes/file.js file, a model and action are specified and the model property of the controller is set to the model. The controller's model property can then be accessed by the template for rendering.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash urls are urls that include a hash (#). Content before the hash is the location
of the document and content after the hash generally references something inside the
document. The content to the left of the hash is loaded by the browser, but the
content to the right is searched for by the browser after content load.

What to be aware of? You need to set up the config/environment.js with a baseURL and make sure to not prefix paths with / since those refer to the full path on the HTTP server and not the path relative to the specified baseURL.

To use the history API instead of hash: configure the application to serve the
entire Ember application to all routes and set the option to history in
config/environment.js under ENV.locationType
```
