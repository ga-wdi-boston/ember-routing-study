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
When the URL change, the ember router will render a template or redirect to a new route.

router => route; route.js => model; template => view
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
hash URL include the route /#, it will load the app to starting state.

when deploy a ember app, those things should be prepared:
1 image data should be referenced with a relative path;
2 config/environment.js should contains ENV.baseURL and ENV.locationType;
3 build the project to dist/;

If using history url, you need to set up the server to make sure it will response the request, like in Rudy, you can set the route in routes.rb.

http://discuss.emberjs.com/t/location-history-feature-and-unbookmarkable-route-urls/1248
```
