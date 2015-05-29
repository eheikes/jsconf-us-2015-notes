# "You Won't Believe This One Weird Way to Rewrite Closures" by [Jonathan Martin](https://twitter.com/nybblr)

This talk was an exercise in writing a closure implementation in JS from scratch.

Most of this talk was live coding with TDD. The best way to see how it works is to check the [code repo](https://github.com/nybblr/closures) or the [interactive transpiler](http://nybblr.com/closures/).

* Rewrite closures, sort of like the way React rewrites the DOM with its virtual DOM
* Ground rules
  * No variables or function parameters
  * No memoization (functions are amnesic)
  * Can access a single global variable
  * Shortcut for setting/getting local variables
* API
  * `s(name, val)` to set a variable
  * `g(name)` to get a variable's value
  * `f(name, params, body)` to create a function
