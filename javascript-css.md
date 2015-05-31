# "Javascript CSS" by [Parsha Pourkhomami](https://twitter.com/parshap)

This talk was about writing CSS using JS. "This talk is about ideas, not code."

* Limitations of CSS
  * No constants or variables
  * No extensionability
  * Bad dependency management
  * No code sharing/reuse (modules)
  * No interoperability with JS
* Preproccessors
  * Ambiguous syntax
  * Nonstandard semantics
  * Still not a real (i.e. Turing complete) language
  * They have their own messiness, with weird behaviors/gotchas.
* Define CSS as JS literals
  * Example:
        ```javascript
        '.nav': {
          color: 'blue',
          fontSize: '1.5em'
        }
        ```
  * Could have something like `toCSS()` to convert the JS object into a CSS string
* JS addresses all the limitations of CSS (see above)
  * Can use npm modules
  * Can use math & JS built-ins
  * Can use JS syntax
* With great power comes great responsibility.
* Taking it further
  * Transform and inject the CSS into the site. Parse & stringify the CSS AST.
  * Take over the browser -- apply styles to elements manually.
  * Add support for [`@supports`](http://www.w3.org/TR/css3-conditional/#at-supports). Create polyfills.

"Reimplement the browser in the browser."
