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

## Additional Sources

[Gawker's Big Mistake](http://www.webmonkey.com/2011/02/gawker-learns-the-hard-way-why-hash-bang-urls-are-evil/)
[Quora question on hashbangs](https://www.quora.com/Are-hashbang-URLs-a-recommended-practice)

## Ember and URLs

In your own words, how Ember "stops breaking the web".

```md
The use of hashes in a url severes the connection with the server. When a page loads
what happens is that javascript tells it to scroll to whatever is being called.
If javascript were to ever go down, then nothing will render. Ember stops this
through the use of a router to load certain parts of the page based on the
url that is passed to it.  When the url is changed given the user interaction,
Ember will send requests to the server for data that is needed to generate the
appropriate model and template for the view.
```

## Ember Routing

How does Ember use the URL to load view-state? Which layers in Ember are
responsible for which tasks?

```md
Ember uses the router to listen to what URL is being passed in, then it routes
to the proper route and from there the model function hooks the data and puts
it into a template.  The template then renders the appropriate view onto the page
given the url.


```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
Hash URLs are used by javascript to load a page without fully connecting to the
server. In GitHub pages you need to be aware of how you reference images there
are specific formats to how you list it in CSS and embed into templates. The
you want to set up your environment.js file.

Not going to lie still a little be confused on how ember doesn't break the
internet.  Because in my mind I see ember doing almost the same thing as the
hash except the only difference is it uses the router to maintain url integrity.
Maybe this will be covered more in class.
```
