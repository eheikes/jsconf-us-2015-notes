# "The Hybrid Backbone & React App" by [Peter Piekarczyk](https://twitter.com/peterpme)

This talk was about the gradual migration to React and being in between frameworks.

([slides](https://speakerdeck.com/ppiekarczyk/the-hybrid-backbone-and-react-app))

* Previous situation
  * Backbone + Chaplin (like Marionette) + Brunch (build tool)
  * More SPAs & APIs resulted in trouble scaling up the UI
* Specific problems
  * useless re-rendering of the DOM
  * longer load time
  * dev & user complaints
* React benefits
  * reusable components
  * efficient diffing
  * declarative style
  * less mental overhead (templates & views are together in JSX)
* Results
  * happier backend devs -- UI is separated
  * code is more manageable
  * CSS is tied to a component
  * no magic, just good JS
* Piecemeal migration process
  * Start with small components
  * Use a Backbone/React Mixin
  * Familiarize yourself with the APIs (Backbone -> React)
  * Convert the Backbone parent view to use `React.createElement()` instead
* React Backbone Adapter -- integrating React into Backbone+Chaplin
* React Backbone Wrapper -- gets rid of Backbone view & Chaplin
  * passes down data (models/collections) to React props
  * Backbone React Component Mixin
* Gotchas
  * They use Coffeescript (CJSX). Babel/ES6 is much more robust.
  * Implicit returns -- a series of components must be wrapped inside a parent `div`
  * (CJSX) event handlers need to `return false`, otherwise React will emit a warning
* Final thoughts
  * This is interim. They are moving to Flux+React.
  * Also check out [jhudson8/react-backbone](https://github.com/jhudson8/react-backbone).
