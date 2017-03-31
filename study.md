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
When taking advantage of the browers history ember uses the the API history,
meaning what was on the privios 'page' and what is on the current page.
The MDN documentation on history says that several of the methods were never
avaialable to web content. Hash which used anchor based urls like we are familar
with seeing in html markup. There is also none which does not update the url at all
Ember naturally uses auto but that is up to negotiation if the developer wants to
alter that. You can do so by adjusting ENV.location type. Otherwise the router.js
file would handle the manipulation of the url
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash urls are routes that are created with this syntax: In the router example
above, entering /#/posts/newWhen using gitub pages for deploy it is important
the environment file the ENV.locatiionType is set to hash. IF it is not it
will not deploy properly. Also not placing a / before the path/to/file is
equally as important since it is a full path on the HTTP. When using a history
API you need to change the nev.location to history. It also seems like the url
might have trouble, which needs to be corrected by always ensuring that it will
load index.html
```
