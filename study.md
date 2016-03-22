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
Javascript-based SPAs broke the web by putting entire web apps within a single URL.  As a result, people are unable to share specific portions of content or use the back button.  Ember's routing and urls solve this problem by setting content under specific routes / urls, allowing people to share specific content (or states) in apps instead of the whole thing.  Ember saves states, allowing the back button to be used again.
```

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
Route loads the model which contains data
URLs link data

URLs can contain route names, which are used to load view-states.  Specific route names are tied to specific view-states.  Ember is constantly listening to events, and when the correct url containing the route name is entered, it's fired as an event that Ember knows to retrieve the corresponding view-state.

In Ember, the model contains the data, and the routes are responsible for loading the appropriate model.  A model hook is used in the route handler.  The model hook will return Ember Data (promises), a JavaScript object, or an array.  This can then be used in your template or controller, which is responsible for what data is displayed, and how it's displayed.
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs are URLs that contain a hashtag (#), which loads the starting state of the application and allows you to move around the site while keeping the app state in sync. Example:  #/posts/new  takes you to posts.new route.

If you want to use the browser's history API, you need to make sure the Ember app is served from all URLs defined by your Router.map function.  If a user manually types the url (ex: /posts/new), you will need to configure your server to respond to it, since Ember will not do it for you.  You will also need to specify the location as 'history'.

```
