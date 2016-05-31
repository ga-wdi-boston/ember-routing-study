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
Ember uses the URL to find the correct model and template to load. The router for the indicated route reads the URL and uses the model hook which returns Ember Data (or POJO, etc). After the data is finished loading, the template is rendered.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs use anchor-based URLs to load the starting state of the application and keep it in sync as you move around the page. For example: #/posts/new takes you to the posts.new route.

Some things to be aware of when deploying...
* Don't prefix image paths with /, since this is a full path on the HTTP server (not relative)
* Ensure that config/environment.js contains the right info:
    if (environment === 'production') {
      ENV.baseURL = '/project-name';
      ENV.locationType = 'hash';
    }

The history URL use's the browser history API to produce URLs with a structure like /posts/new. Your server must serve the Ember app from all the URLs defined in your Router.map function in case the user navigates directly to e.g. /posts/new.
```
