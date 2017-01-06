# Ember Routing Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Ember.js - Routing: Specifying a Route's Model](https://guides.emberjs.com/v2.5.0/routing/specifying-a-routes-model/)
-   [danwebb.net - It's About The Hashbangs](http://danwebb.net/2011/5/28/it-is-about-the-hashbangs)
-   [Ember.js - Configuring Ember.js: Specifying the URL Type](https://guides.emberjs.com/v2.5.0/configuring-ember/specifying-url-type/)
-   [Deploying Ember CLI apps to GitHub Pages](http://osxi.github.io/ember/github/git/2015/09/22/ember-cli-apps-on-github-pages.html)

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
With Ember the router parses the URL and, in doing that, determines which model to pass it to.  The model
then retrieves the appropriate data and loads it into a template which is presented to the User.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
A hash url contains a 'hash' in it to instruct the router what to do with it.  And example of this would be
http://rick.com/#/coolstuff.  A major thing to look out for when deploying to GH pages is how images are
called (especially those embedded in templates).  The path must not start with '/' but instead look something like
'assets/images/rick.jpg'.

If you choose to use the 'history' API instead of a hash you need to make sure that your server is set to handle all
defined URLs.
```
