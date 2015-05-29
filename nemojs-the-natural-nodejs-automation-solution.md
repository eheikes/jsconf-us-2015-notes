# "NemoJS: The natural nodejs automation solution" by [Matt Edelman](https://github.com/grawk)

This talk introduced [Nemo](https://github.com/paypal/nemo), a way to do end-to-end testing.

* Background
  * Rransformation at PayPal from Java -> NodeJS
  * Needed a way to automate testing
* Nemo is a wrapper for [Selenium](http://www.seleniumhq.org/) / WebDriver
  * JSON config through [confit](https://github.com/krakenjs/confit)
  * starts WebDriver
  * initializes plugins
  * provides access to the WebDriver API
  * still need a test framework and runner
* Simpler code to get Selenium running
* Provides access to WebDriver API -- `nemo.driver`, `nemo.wd`
* Confit + [Shortstop](https://github.com/krakenjs/shortstop) handlers
  * syntax to point to environment variables, a file, argv, etc.
  * multiple configurations possible, looks at the environment (`NODE_ENV`)
* What can go in plugins?
  * WebDriver abstractions
  * user interactions
  * proprietary functionality
* [`nemo-view`](https://github.com/paypal/nemo-view) plugin
  * provides a way to work with elements on the page
  * `_find()` & pass it a CSS selector
  * use a JS object to define locator methods, e.g. `nemo.view.nav.bank().click()`
  * helps you create "flow files" -- pattern to put workflows into modules
