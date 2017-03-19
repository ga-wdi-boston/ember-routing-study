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
Ember uses a url to indicate which view-state to display.  The routing layer defines a specific route (using the URL).  A URL can show a template model which varies depending on the url.  For dynamic models, models change due to user interaction.  Ember extracts a defined route with dynamic urls which is passed to the value is passed as a hash for the model hook.  Once this occurs, a specific model hook returns an ember data record) and a specific viewstate is achieved.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Example hash URL: http://2011.jsconf.us/#!/schedule

Hash urls uses the url anchor to load the original state of an appolication and it keeps various starting states synchoronized as the user interacts with the application.

History APIs use the bowser's history API to produce a URL.  If you want to use a history API, you need to take account of this in the appilcation router using the map method.

When preparing to deploy to github it is important to not use a path with / because it is a path to TTP server (not relative).  After building using the command "ember build --environment production", one can deploy to github.  At this point, a gh-pages branch will need to be created, a copy of the app build must be located in the root of a repo, relevent files must be added and this all must be pushed to github.
```
