# "Introducing Mixed Mode" by [Mike O'Brien](https://github.com/michaelobriena)

This talk introduced the new "mixed mode" in the [Famous engine](http://famous.org/).

* Unifies the DOM and WebGL
  * one API
  * one coodinate space -- everything's in pixels
* Why
  * DOM is familiar to users and devs
  * WebGL lets you make pretty stuff
  * Represents multimedia content (text + graphics), but it's more than just an overlay.
* Behind the scenes of the compositor
  * 2 DOMS: WebGL (canvas) and page DOM
  * Canvas is always in front. Cutouts are used for correct z-rendering.
* Demos
  * WebGL representation of an opened Macbook, with a navigable webpage displayed on the laptop's screen.
* Limitations
  * Currently rectangular DOM only
  * A few other minor ones
* Happy accidents
  * Can run separate from the normal UI thread (e.g. in web workers)
* Summary
  * Think outside the document. Treat your page as a DOM of scenes.
  * 2D layout is a subset of 3D, so define everything in 3D.
  * Abstract away the renderer.
  * Thin clients give flexibility.
