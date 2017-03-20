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
A template displays data from a model through a router. The router has a route
defined which accesses a particular data set from the model. The model returns a
Ember Data record and possibly a promise object and a plain javascript object or
array before rendering the template with the requested data.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs are an optional part of the URL that is after the # and identifies
a portion of that document. When using GitHub pages to deploy the Ember app
URL paths should not be prefixed with a / and images in CSS files should be
formatted like url('images/foo.png') and in templates should be formatted like
assets/images/foo.pn. Also config.js needs to include:

if (environment === 'production') {
  ENV.baseURL = '/project-name';
  ENV.locationType = 'hash';
}

If one wants to use the history API instead of the hash for location one would
need to change the ENV.locationType to `history`.
```
