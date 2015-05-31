# "Accessibility and JS" by [Felipe de Albuquerque](https://twitter.com/felipedeolinda)

This talk was given in Portuguese (with English translator) to demonstrate what it's like to access content through an intermediary.

([slides](http://www.slideshare.net/FelipeAlbuquerque/accessibility-and-js-sidebyside))

* Why is accessibility important?
  * 650 million people have some sort of disability.
  * We want to include as much of our potential audience as possible.
* What is "accessibility"?
  * Making site accessible (available and usuable) to the most people.
  * Enabling disabled people to use the site.
* Who needs accessibility?
  * People without or less sight
  * People with poor mobility (hands)
  * People on the colorblind spectrum
  * Children/kids and older people
  * Hearing impaired
* Current documentation / initiatives
  * W3C, [WAI](http://www.w3.org/WAI/), [WCAG](http://www.w3.org/WAI/intro/wcag), [WAI-ARIA](http://www.w3.org/WAI/intro/aria.php), [ATAG](http://www.w3.org/WAI/intro/atag.php), [UAAG](http://www.w3.org/WAI/intro/uaag.php), eMAG
* 4 principles of WCAG
  * Perceivable
    * Distinguishable info
    * Provide text alternatives for non-text content.
    * Adaptable
    * Time-based media
  * Operable
    * Make the site usuable with a keyboard.
    * Don't have content that moves/blinks enough to cause seizures (3 times per sec).
    * Give users enough time to use controls.
  * Understandable
    * Specify the human language of the page.
    * Use good writing and appropriate reading level.
  * Robust
    * Compatible with all kinds of user agents
* User agents <img src="https://i.imgur.com/7pOwI.jpg" alt="Funny cartoon used in his slides" width="350" align="right">
  * Handicapped people often use screen readers (text-to-speech) such as JAWS, NVDA, VoiceOver, etc.
  * Screen reader usage on mobile phones has been rising -- currently at 82%
  * Use good HTML: correct `doctype`, a `lang` attribute, `meta` tags
* Barriers
  * Biggest website issues
    * Browser has no JS support or it's disabled
    * Devs lack ARIA knowledge
    * Rich content/interaction ([RIA](http://en.wikipedia.org/wiki/Rich_Internet_application))
    * No keyboard accessibility
  * No JS
    * 97.6% of browsers support JS. For those that don't, provide alternative controls.
    * Detect features instead of browsers/versions.
  * Lack of ARIA knowledge
    * ARIA makes RIAs more accessible.
    * ARIA is an accessibility API that provides info to assistive technology.
    * It's already implemented/available in browsers.
    * ARIA live regions for Ajax accessibility: `aria-live`, `aria-relevant`, `aria-describedby`
  * Ability to navigate with a keyboard
    * Link text should convey the purpose of the link (not just `<a href>here</a>`).
    * Provide "skip navigation" to bypass content (e.g. go straight to main content).
    * Use CSS `:focus` outline. Use JS to set `focus()` and scroll to elements.
    * Provide keyboard shortcuts.
    * Use `aria-label` etc.
    * Hide submenus and show them on `focus`.
* Secrets
  * Provide a menu specifically for accessibility with controls for font size, contrast, etc.
