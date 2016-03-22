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
Because Ember utilizes the MVC framework, using unique routes and URLs is inherently baked into the process of creating a web application using Ember.
```

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
Ember uses the URL to route to render a certain template. The route handler can control weather to load a template or a model that is then displayed through another template.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs ensure that certain operations are executed when a specific URL is entered regardless of extra text that may be part of the HTTP request. Excess text is invisible to the server and is left up to the programmer and javascript syntax to ensure the desired task is completed correctly.
When using the history API to produce URLs the route uses anchor based URLs, while the hash option can anchor the route with a hash to alow for the application to stay in sync when move around to another serve with different URLs. The has option needs to be set as the location in order for the application to correctly work while hosted on Github.
```
