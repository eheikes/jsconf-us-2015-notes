# "Build the Mobile Web You Want" by [Kate Hudson](https://twitter.com/k88hudson)

* "The web is broken" -- mobile is becoming the first & dominant method people use
  * Expected features: performant UI, seamless auth/security (typically email confirmations for the web), works with offline/intermittent network, device/OS integration (camera, push) <img src="http://image.slidesharecdn.com/k88hudsonjsconf-150527152747-lva1-app6892/95/build-the-mobile-web-you-want-6-638.jpg?cb=1432740600" alt="comparison between web and native of expected features" width="350" align="right">
  * Web browsers are getting better, but native has the advantage. Concede defeat?
* Remember that in 2004, making a JS/Ajax app was not a thing, and even criticized. Gmail was the killer app -- a "hack".
* Proposal: "It is time to hack."
* First Level of Hack
  * Test new browser features before their time (e.g. service workers).
  * Transpile
  * Polyfill
* Second Level of Hack: Build new abstractions
  * Create DOM abstractions/augmentations (e.g. React, [Famous](http://famous.org/)).
  * Create things that don't exist on the web (e.g. [filer.js](https://github.com/ebidel/filer.js/)).
* Third Level of Hack: Blow shit up -- hack the user agent
  * Build hybrid apps (e.g. with Cordova).
  * Results of android testing in Kenya, India, and similar countries
    * Problems
      * poor offline experience
      * mem leaks in long-lived processes
      * UI performance
      * Android <4.4 stock browser is horrible
    * Have the app use an embedded [WebView](http://developer.android.com/reference/android/webkit/WebView.html) or [Crosswalk](https://crosswalk-project.org/)
    * Expose custom Java interfaces to JS. In the example app:
      * moved the apps's Router, SharedPreferences into Java
      * saved app state in Java; React hooks into it
      * exposes device integration (camera, offline caching, gestures) to JS

"Build the web you want". Really good engineering is finding adequate solutions to problems that matter in a way that someone in the future can understand and improve on.
