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
The router parses the url to determine which view-state to load, and uses that information to query the appropriate model, and then loads the info from the model into the template in order to render the appropriate view state
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
a hash URL is one of these: /#/posts/new

make sure that you have images referenced in a path like `assets/images/foo.png`

make sure that the base url doesn't start with a /

and make sure your config/environment.js contains this:

`if (environment === 'production') {
  ENV.baseURL = '/project-name';
  ENV.locationType = 'hash';
}`

to use `history`, you need to make sure that your server is configured to handle all the defined URLs, even if the client navigates there directly
```
