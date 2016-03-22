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
Ember "stops breaking the web" is about getting back into using URLs.
Tom Dale expresses the need to start using urls again instead of using hash URLs.
Ember actually renders the page according to the url.
It will acutally update the MVC according to the url.
So for a multipule MVC page to have each MVC to be updated seperatly this can be done through URLs.

```

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
Ember uses the url to load a view-state when the router gets hit then goes to that routes file and loads the model then the template will render.
The router is responsible for parsing the url to see if a route exists.
If the route does exist ember then will look for the file in the routes folder that matches the parsed url and then will exescute the model in that route.
When the data comes from the model it will then be renderd in the template.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md

A Hash URL is like `http://thingy.com/#/posts/1/history`. They have `#` in the URL.

It's important not to prefix image data with a `/`. You must add an if statement saying if the environment is a production environment then change the base url to `/project-name` and set the locationtype to `hash`.
You also need to be aware that you want to copy the compiled data from dist. then push to gh-pages.

If you want to use the history api insted of a hash for location all you have to do is set `ENV.locationType` to `history`.

```
