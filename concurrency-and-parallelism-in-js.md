# "Concurrency & Parallelism in JS" by [Naveed Ihsanullah](https://twitter.com/naveedi)

([video](https://www.youtube.com/watch?v=h_M_uscOKJM))

* Concurrency & parallelism <img src="https://pbs.twimg.com/media/CGCoz7hXIAA2kzb.jpg" alt="Analogy of difference between concurrency and parallelism" width="350" align="right">
  * Concurrency is having multiple tasks run together (multitasking)
  * Parallelism is actually executing tasks separately (in hardware)
* Browser implementations of JS is fast and getting faster with asm.js etc
* Parallelism is bottlenecked by the hardware, and concurrency is bottlenecked by waiting on responses.
* Improving parallelism
  * [Web workers](http://www.html5rocks.com/en/tutorials/workers/basics/)
* Improving concurrency
  * [Parallel JS](http://adambom.github.io/parallel.js/) -- still experimental etc
  * [`postMessage()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) -- performance isn't there
  * transfer buffers around
* Native has solved this. Do similar on the web: [shared memory for JS](https://blog.mozilla.org/javascript/2015/02/26/the-path-to-parallel-javascript/)
  * `postMessage()` + `SharedArrayBuffer`
  * use `SharedInt32Array` to view on it
  * the low-level details can be abstracted
* Availability
  * Landed in Firefox Nightly.
  * Announced for future Chrome too.
  * Unfortunately can't be polyfilled.
