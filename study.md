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
<!-- your answer here -->
Embers router helps us to stop breaking the web.  With ember we get URLs and a working back button.  Ember allows you to
stop putting your whole application under one URL.  Best practices are essentially built in.  Allows you to manage a large codebase with a many people being apart of
the team.

```

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
<!-- your answer here -->
4 basic parts to an Ember app.  Router/routes, model, service, componants
  Ember uses the routing layer choose a model based on the URL.  Then a componant takes over for display and user
  interaction.  A service (data store) may be used to retrieve models.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
<!-- your answer here -->
URLs link one piece of data to another. The hash option uses the URL's anchor to load the initial
state of your app.  It will keep your site in sync as you move from view to view.  Your app uses the browser's history
API to procduce URLs with the structure /something/something-else.  If history is not supported by the browser, the app
will fall back to hash.  When deploying to git-hub pages you must be aware of the build process.  You must make sure you
run ember build --enviroment production and build the project to dist/.

```
