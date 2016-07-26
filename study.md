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
<!-- your answer here -->
The URL is parsed by the router, which goes to a specific route. The route is connected to a model. Models return some kind of data (or promise object, or plain object), which is then hooked into a template. All together, those things are how Ember uses a URL to load a view state.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs use an anchor to load the starting state of the application from the server
 and keep it separate from the client-side url used by Ember (after the hash).
(https://guides.emberjs.com/v2.5.0/configuring-ember/specifying-url-type/)

If using github pages for your deployed Ember app, you need to make sure that path names
don't start with a / because that would be read as a full path by github, instead of a relative
path within the app itself (and thus it won't be able to find it.)
(http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

```
