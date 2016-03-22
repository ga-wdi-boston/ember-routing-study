# Ember Routing Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Watching

-   [CascadiaJS 2013 - Tom Dale - Stop Breaking the Web - YouTube](https://www.youtube.com/watch?v=BQ6at0addi4)

## Required Readings

-   [Ember.js - Routing: Specifying a Route's Model](https://guides.emberjs.com/v2.4.0/routing/specifying-a-routes-model/)
-   [danwebb.net - It's About The Hashbangs](http://danwebb.net/2011/5/28/it-is-about-the-hashbangs)
-   [Ember.js - Configuring Ember.js: Specifying the URL Type](https://guides.emberjs.com/v2.4.0/configuring-ember/specifying-url-type/)
-   [Deploying Ember CLI apps to GitHub Pages](http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

## Ember and URLs

In your own words, how Ember "stops breaking the web".

```md
Single-page apps are great, but they (usually) lack URLs. URLs are useful for sharing,
collaborating, and forking content, so without them the web becomes less useful. Ember
deals with this by providing URL-linked resources within single-page apps.
```

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
The first portion of the URL corresponds to the model, with the second portion
corresponding to the specific method of that model. From there, the router will
render the handlebars template of the same name as the specific method into the
{{outlet}} of its parent route's template.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs use # anchors to load the starting state of your app. When using github pages,
it's important not to prefix paths with '/', because that's the full home path, and
these resources may or may not be located relative to that path. If you want to use the
'history' API, you need to keep in mind that not every browser supports it, so some of
your users may end up falling back to 'hash' anyway.
```
