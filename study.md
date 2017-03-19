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
the hash can detemine the view-state.
The router with a hash preceding it like /#/routeName will make a new route. The history
part is for the browsers history and the hash is for a certain part in the application
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
I think it takes you to certain part of a route, like a certain part on a page.
When deploying make sure not to precede routes with a slash "/" for css, as ember will see it as
an absolute path, and to look at the app name base url to make sure it DOES precede with a slash. Also in deployment
make sure to look that locationType has 'hash' for a value. In order to change API to history, you would change
'location' s value to 'history' from 'hash'
http://emberjs.com/api/classes/Ember.Location.html
```
