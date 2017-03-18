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
The Ember router defines any number of given routes. When a route is hit it uses a route-handler which can load the appropriate model. Using the return value of the route handler's `model()` function, a `model` property will be set for the controller which will allow templates to access the model's data. Dynamic or specific content can be accessed using this system by defining `params` in the route and passing those params to the `model()` function in the route handler.
```
https://guides.emberjs.com/v2.11.0/routing/specifying-a-routes-model/

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs are a way of maintaing state in a front-end application. When URLs use hashes the content specified after the hash is not sent to the server.

When deploying to GitHub pages it is important not to prefix URLs for assets with `/` as this will not use the `ENV.baseURL` property. To get the app ready for production the `ember build --environment production` command should be use to build assets into a `dist folder.`

If you want to use the history API your server must be configured to serve your ember app rather than content matching that route.
```
http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html
https://guides.emberjs.com/v2.11.0/configuring-ember/specifying-url-type/
http://danwebb.net/2011/5/28/it-is-about-the-hashbangs
