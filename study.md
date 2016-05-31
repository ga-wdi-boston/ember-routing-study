# Ember Routing Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Ember.js - Routing: Specifying a Route's Model](https://guides.emberjs.com/v2.4.0/routing/specifying-a-routes-model/)
-   [danwebb.net - It's About The Hashbangs](http://danwebb.net/2011/5/28/it-is-about-the-hashbangs)
-   [Ember.js - Configuring Ember.js: Specifying the URL Type](https://guides.emberjs.com/v2.4.0/configuring-ember/specifying-url-type/)
-   [Deploying Ember CLI apps to GitHub Pages](http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
Ember uses dynamic segments in the URL, which are routes that specify which template to display
along with which model to use. The router is responsible for the resource name
and the path, the routes use a model hook, which should return Ember Data(or a promise),
the data from the route then gets rendered in a template.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md

Hash URLs are fragment identifiers that send a series of related requests that are
processed under the same URL and it is used as a way for dynamically adding functionality
on web apps. It's also a way to display different variations of the content on the same page.
Devs throw the parameters after the hash and then Javascript is used to interpret the message and
render the content mandated by the params.

You need to ensure before deploying to GH Pages that all your file paths are not prefixed with a
'/'. Then you need to ensure in your config file/environment.js file includes the env.base URL and
the location type. Then you run the build CLI to dist/, which then you must copy the app to the root of the
repo. Finally, add relevant files and then commit/push.

If you want to use the history API, then both client and server must be configured to handle Ember.


```
