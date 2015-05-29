# "Tungsten.js: Virtual DOM & Server Rendering in a Legacy Codebase" by [Andrew Rota](https://twitter.com/AndrewRota) & [Shrenik Sadalgi](http://www.shreniksadalgi.com)

This talk was about improving a legacy codebase without rewriting it from scratch.

([code repo](https://github.com/wayfair/tungstenjs))

* [wayfair.com](http://www.wayfair.com/)
  * ecommerce site for home items
  * PHP + JS
* What they're doing right
  * Mustache templates with C++ extension in PHP
  * Lazy loading
  * JS bundling
* Room for improvement
  * jQuery + Backbone = slow DOM manipulation and over-rendering
  * Devs overuse direct DOM manipulation
  * Devs have to know the low-level performance of DOM methods
* Next step?
  * Looked at Ember, Angular, React
  * Would require complete rewrite of code -- expensive, stalls other development, and might not finish
* Characteristics of legacy code
  * Existing tech stack
  * Old frameworks/libs
  * Technical debt
  * *It works*
* "Remodel the kitchen without tearing down the whole house"
* Had:
  * shared templates
  * fast server processing
  * Backbone
* Wanted:
  * fast client-side rendering (vitual DOM)
  * no DOM manipulation
* Piecemeal improvements
  * Use [Ractive](http://www.ractivejs.org/) to precompile Mustache templates into objects, not strings.
  * Use Mercury's [virtual DOM](https://github.com/Matt-Esch/virtual-dom) library.
  * Use Backbone to bind events and handle the data layer.
  * Write integration library to pull it together: [TungstenJS](https://github.com/wayfair/tungstenjs)
* This was for a specific situation.
  * It's not an SPA.
  * Analogy: Farmers in remote areas used an existing infrastructure (barbed wire) to wire up telephone service.
* DBMonster perf test
  * Comparable to React, Ember+Glimmer
  * The [Paperclip library](http://paperclipjs.com/) is really fast and does something similar.
