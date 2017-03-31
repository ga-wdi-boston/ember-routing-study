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
It's the job of the URL and routes to load the appropriate data from the model
to display in the view-state's template. The route handler uses a model hook
to retrieve data from the model and set it as the model property of the controller.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs are anchor-based URLs, that use the anchor of the URL to load the starting
state of the app and then keep it in sync as a user moves through the page. Any data
that comes after the # is not sent in an HTTP request - it's invisible to the server, essentially.

To specify how we manage an app's URL, we go into config/environment.js in our app
and set the ENV.locationType. For deployment on github pages, this _must_ be set
to `hash`. If we want to use the `history` API, we need to make sure that our app
includes a route for `/location` and can serve that route if the user navigates
there directly.
```
