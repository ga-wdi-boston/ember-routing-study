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
Ember uses the URL to load view-state by extracting the value of a dynamic
segment from the URL. This path structure is defined in the router. This value
is passed to the model hook in the appropriate route. From there, the correct
data is retrieved and shown using the associated template.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs utilized a hash symbol in the URL to avoid page reload, and contain
information after the # which is used by Javascript to decide which content to show.
This approach is a hack created before the history API was widely supported.
When using GitHub pages for your deployed Ember app, hash URLs should be used.
The history API is actually used by default for location when set to auto. It
falls back to hash URLs if history is not supported by the browser. To use only
history, set ENV.locationType to history in config/environment.js.
```
