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
What content will be loaded by a given URL is determined by the router/route handler
and the model in ember. We define what the URL to watch for in the router. The route
handler for that URL then uses a model hook to pull model data, allowing you to
access it from within your template which will update your view-state

- Router identifies URL
- Route handler call correct model hook.
- When hook resolves, model is passed to controller ???
- You now have access to data from within your template
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLS are URLs that don't actually map to any data on the server side. The
Frontend javascript looks at the string after the # and determines which content
to load.

Image paths need to be set correctly when deploying to gh-pages. There cannot be
a leading / in the path.

By default ember uses the auto feature for URLs. To change this you have to change
the setting config/environment.js under ENV.locationType.
```
