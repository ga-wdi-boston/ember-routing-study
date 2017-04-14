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
In Ember, each view state is represented by a URL.  When a URL is requested, the corresponding route loads that view state with the associated model and data.  I'm unsure of how the second part of this questions differs from the previous study in which we described routes, models, templates, components and services.  The layers which are most directly related to using the URL are routes and models for the above reasons.

(sources:
Friday's session
https://en.wikipedia.org/wiki/Ember.js)
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URL's (also known as fragment URLs) are URL's segmented by a hash with a resource to the left of the hash and a location within the resource to the right.  When accessed, they direct the browser to that location within the page.

Wen using GH pages to deploy, image data paths should not be prefixed with '/' as a full path on the HTTP server is being accessed rather a relative one.  The file config/environment.js should also be updated according to the instructions found at 'http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html'.

You wouldn't have to change anything to use the 'history' API instead of 'hash' since Ember defaults the router to use 'auto' which in turn uses 'history' if supported by the user's browser and 'hash' if not.  Changes to this configuration can be made in the file 'config/environment.js' under 'ENV.locationType'.     

(sources:
https://blog.httpwatch.com/2011/03/01/6-things-you-should-know-about-fragment-urls/
http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html
https://guides.emberjs.com/v2.4.0/configuring-ember/specifying-url-type/)
```
