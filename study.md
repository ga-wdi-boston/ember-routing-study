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
Ember loves URLS and so should you. You've been breaking the internet because
you're a hot shot JS dev who uses client-side frameworks and hashbang
URL's to load current-state and navigates easily cuz jQuery bro. But your hashbangs
and terrible URL's are slowing down your users experience (especially those with older
browsers, who don't even want your fancy new feature's that won't load) and making it
hard for people to know where to go to get to your website. Good luck having some
one bookmark your page.
```

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
Ember uses the URL to determine which route to use to get to whatever routing handler
is associated with the model that the client would like to interact with at the
time to display whatever data in the current view-state.

The router and routing layer are responsible for communication with the model. The
model is responsible for actually spitting out the correct data and the
corresponding template.hbs file is responsible for actually rendering the different
components in the view-state.

```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
  A hash URL makes sure that starting state of the app is loaded and kept up to
date as you move around and interact with the app.

  When deploying to GH pages, it's important to make sure your environment
variables point to the proper project name and the proper location API for
URLS. Also make sure to load all necessary file paths into the /dist folder in
order for gh pages to properly build your app.

  To use the 'history API instead of hash change your config/environment.js file
and set the location to history like so:

if (environment === 'production') {
  ENV.baseURL = '/project-name';
  ENV.locationType = 'history';
}
```
