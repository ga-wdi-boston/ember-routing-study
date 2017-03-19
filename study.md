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
The router parses the URL and and matches it to the routes that are defined.
The routes are responsible for loading the appropriate model, displaying
templates, etc.
To load a model for a particular route, it invokes its model() hook, in which
our app returns a model.
It then renders the component, passing it the resolved model item.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs are URLs with a hash(#) sign separating the server side URL portion
from the side used by ember.

To deploy to gh-pages -
In the production environment, set the base URL, and the location type to
'hash'. DO not prefix the path with '/'.
Build the prod environment to /dist.
Copy the app to the rot of the repo.
Add files, commit and push.

When using 'history' API instead of 'hash', use /posts instead of /#/posts
```
