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
The view-states are are simply templates which may or may not display data from a model.
It's the URL (or routes) job to load the appropriate model.

https://www.aeturnum.com/warming-up-ember-js-2/

Ember is comprised of 3 main layers: the controller layer, the view layer, and
the model layer.
The controller layer is built with a combination of routes and controllers.
The view layer is built with a layer of templates and views.  It's responsible for user events, and updating the DOM structure when the data of the view changes.
The model layer is built with a combination of model and ember data.responsible for any server side communication and data formatting.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
I'm having a great difficulty in finding any other sources on these quetions.  The sources
provided aren't really clicking. I'm confused about the use cases for each URL type, especially
the `hash` url.  
```
