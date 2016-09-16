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
For each view state, appropriate model has to be loaded. Each model holds the data, and that data is loaded by having the appropriate route. To load data for each view state, we would use model() hooks that would let us access model property in the controller, which would let us access controller property in the template, and then template will render the data for each view state.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs load starting state of the application and it will keep it sync as user moves around. URLs aren't meant to be changed, but sometimes data needs to be deleted or domain name needs to be changed. If we are using non hash URLs we can handle changes using HTTP. If content is deleted, we post a page with a message, or if content is moved to a different location, we post a message about that too.

With # URLs that isn't possible because the part of URL after the # is considered as specific content and it isn't even sent to the server. To handle this, we need to use JavaScript to examine that portion of URL after the #.

If we want to use history API instead of hash, we would need browser's history to produce URL.
```
