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
The router, taking over from the browers on a url navigation, describes a list
of routes that are appended to the root url (example: www.something.com/ + route).
The model for that route then takes over and returns promises. These promises
resolve as the return value for the model in the controller, which then can be
rendered in the DOM by the controller.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash urls use a hash after the root url as an anchor for any view-state urls you
may wish to append to it. Being aware of ENV.locationType is important for github
pages deployment, for if you want to use the history API, you have to set
ENV.locationType's value to 'history'. Setting it to 'hash' keeps using hash urls,
while a value of none prevents any url manipulation. Plus, using the history API
requires a user to be able to navigate from the page they land at, even if it isn't
the root (You have to account for this in your Ember app's router).
```
