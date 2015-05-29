# "The Pebble Timeline" by [Charlie McConnell](https://twitter.com/Av1anFlu) & [Lance R Vick](https://twitter.com/lrvick)

In this talk the speakers went over the [Pebble watch](https://getpebble.com/) timeline, how to build for it, and described how they build stuff.

([slides](https://docs.google.com/presentation/d/1k98aBbSss2Net3kooREcyq6ptyerjQ9DqLm5kOB1tq0/edit))

* [Pebble timeline](http://developer.getpebble.com/guides/timeline/): a Pebble interface for upcoming and past life events ("pins")
* To build apps for timeline:
  * Use [pebble-api](https://www.npmjs.com/package/pebble-api) for the server
  * Create an app for the watch that queries the server
  * Example: [JSConf schedule](https://github.com/pebble/jsconf2015-schedule)
* Timeline API
* Their infrastructure: "version controlled immutable deployment" with Docker
  * Deployments driven by git-hooks --see [git-deploy](https://github.com/pebble/git-deploy)
  * Docker has some not-so-good things
  * They use CoreOS (based on ChromeOS, Gentoo) for the server distro. Only software on the server is `dockerd`.
* Deployment pipeline
  * Private Docker registry for building/hosting images
  * A webhook server in staging pulls new images when they complete.
  * A custom repo for production seeds config data into `etcd` and restarts services.
  * 90% bash, 10% Go
  * Docker images are the immutable deployment artifacts.
  * Every server is the output of a program; if misconfigured, fix the program.
* Solving real-world problems
  * ["Is the restroom free?"](https://github.com/pebble/toilet-time) app
