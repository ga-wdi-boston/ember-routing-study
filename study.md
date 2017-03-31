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
When an Ember application starts, the router matches the current URL to the routes
that are defined. The routes are then responsible for displaying templates, loading data,
and setting up the view-state.

In order to load a particular view-state, a template is required to to display data
from the model. One of the tasks of the route is to load the appropriate model.
To load a model for a specific route, you would use the model() hook in that
route's route handler.

The model hook will usually return an Ember Data record, but it can also return
any promise object (Ember Data records are promises), or a plain JavaScript object or array.
Once the data finishes loading (until the promise is resolved) the template is
rendered. The route will then set the return value from the model hook as the model
property of the controller.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs looked something like this: http://whatever.com/path/to/#!/some-ajax-state.
In the past, a link served two purposes: It loaded a new document and/or scrolled down
to an embedded anchor as indicated with the hash (#). After the adoption of AJAX
the hash was used as a sort of "state" reference to be included in links & bookmarks.
After the document loads, the browser reads the hash and runs the AJAX requests,
displaying the page plus its dynamic AJAX changes.

When deploying to GitHub pages you need to be aware of the contents in config/environment.js.
The location type, whether you want to use hash, history API, or none needs to be
explicitly entered in the file. It seems like this is increasingly important during
testing, development or production phases.

To use the history API instead of hash for location, you simply need to type
ENV.locationType = 'history'
```
