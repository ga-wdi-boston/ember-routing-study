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
To load view-state Ember uses dynamic segments - it's a portion of a URL that starts with a

```:``` and is followed be an identifier for ex: ```post_id``` for post,
```comment_id``` for comment.

```app/router.js``` - is responsible  for loading the appropriate model

```app/routers/some-name.js``` - is a route handler and will use the model() hook
 inside that file. model() can return ```Ember Data``` record or ```promise object```
 or a ```plain JavaScript object``` or ```array```.

 ```app/templates/some-name.hbs``` - accesses controller's ```model``` property
 which is a value from the ```model hook``
```

## Deploying Ember

What are hash URLs? What do you have to be aware of when using GitHub pages for
your deployed Ember app? What do you need if you want to use the `history` API
instead of `hash` for `location`?

```md
hash URLs use URL's anchor to load the starting state of the app and sync it when
moving around. - for ex: ```/#/posts/new``` will take me to ```posts.new```

When using GitHub pages for my deployed Ember app - the url CSS datatype should
reference image data with a path like ```url('images/foo.png')```. And images embedded
into templates should reference image data with a path such as ```assets/images/foo.png```.
```foo.png``` for both is an image at ```project-name/public/assets/images/foo.png```.

Then in ```confi/environment.js``` should be
````if (environment === 'production') {
  ENV.baseURL = '/project-name';
  ENV.locationType = 'hash';
}```



URL Type has four options - ```history, hash, auto, none```.
If I want to use ```history``` API instead of ```hash``` for location - Ember uses the browser's
history API to produce URLs with a structure like ```/posts/new``` and it will take
me in the app/router.js to ```posts.new``` .

```
Router.map(function() {
  this.route('posts', function() {
    this.route('new');
  });
});```


```
