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
<!--It uses the components in the url to determine the navagation path. So from the reading if we wanted to go to posts.new the mapping in the url would have /posts/new after the main address. It also at first will load the base site and will adjust data values depending on where you have navagted to or what you have changed on the site. So instead of reloading the page with a new view it keeps the main part loaded while switching the view-state. At least again thats how I read it, I don't think I am grasping the whole topic though. -->
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
<!-- Hash urls are a way to anchor other parts of your content to the main URL without configuring a specific navagation to that part of your content. All your paths have to be mapped out if you're going to deploy with history instead of using hash or auto. Github needs the paths to also be set up to connect the paths from the front end the back end either way. That can be accomplished both manually or automaticly using what git hub has provided for deploying ember applications.  -->
```
