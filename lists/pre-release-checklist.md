Copy and paste into a GitHub issue or pull request and commence testing.

# Pre-release testing checklist

All items need to be checked off before this version of the build can be released into the wild.


## Performance

- [ ] Minify CSS and JS, and remove unused/redundant code [[Read more](https://developers.google.com/speed/docs/insights/MinifyResources)]
- [ ] Compress raster images [[Read more](https://www.html5rocks.com/en/tutorials/speed/img-compression/)]
- [ ] Optimize SVG path data [[Read more](https://web-design-weekly.com/2014/10/22/optimizing-svg-web/)]
- [ ] Make sure styles and scripts are not render blocking [[Read more](https://csabapalfi.github.io/eliminate-render-blocking/)]
- [ ] Install a service worker and cache all applicable assets [[Read more](https://css-tricks.com/serviceworker-for-offline/)]
- [ ] Lazy load large image assets
- [ ] Use `srcset` to tailor images to devices and reduce bandwidth costs
- [ ] Subset fonts to just the characters needed


## Accessibility

### Readability

- [ ] Make sure main body (paragraph) text is no smaller than the default (user agent) size [[Read more](https://www.smashingmagazine.com/2011/10/16-pixels-body-copy-anything-less-costly-mistake/)]
- [ ] Avoid justified body text [[Read more](https://www.w3.org/TR/WCAG20-TECHS/F88.html)]
- [ ] Employ well-balanced, highly legible fonts (not too complex or elaborate)
- [ ] Translate / spell out acronyms the first time you use them
- [ ] Give all form elements permanently visible labels
- [ ] Place labels above form elements
- [ ] Do not use very thin font faces [[Read more](http://www.telegraph.co.uk/science/2016/10/23/internet-is-becoming-unreadable-because-of-a-trend-towards-light/)]
- [ ] Provide enough spacing between lines of text (`line-height`) [[Read more](https://www.w3.org/TR/WCAG20-TECHS/C21.html)]
- [ ] Ensure the same content is available across different devices and platforms
- [ ] Make sure the purpose of a link is clearly described: "read more" vs. "read more about accessibility"


### General accessibility

- [ ] Support "pinch zoom" (remove `user-scalable=no` if present)
- [ ] Include only clear, meaningful animations
- [ ] Give grouped form elements group labels
- [ ] Ensure content is not obscured through zooming (no fixed widths)
- [ ] Mark invalid fields clearly and provide associated error messages
- [ ] Indicate swipe gesture support clearly, and provide simple tap-based alternatives
- [ ] If content is meant to be hidden, ensure it is properly hidden to all users
- [ ] Do not auto focus form fields, on page load


### Support for low vision & assistive technologies

- [ ] Use screen reader and keyboard accessible HTML [[Read more](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)]
- [ ] Give video content captions and transcripts
- [ ] Provide transcripts for audio content
- [ ] Provide alternatives and/or descriptions for complex visualizations
- [ ] Support Windows high contrast mode (use images, not background images) [[Read more](http://adrianroselli.com/2012/08/css-background-images-high-contrast-mode.html)]
- [ ] Provide alternative text for salient images [[Read more](https://www.w3.org/WAI/tutorials/images/decision-tree/)]
- [ ] Apply `alt="` or `aria-hidden="true"` to decorative images [[Read more](https://www.w3.org/WAI/tutorials/images/decorative/)]
- [ ] Make sure text and background colors contrast sufficiently [[Read more](https://accessibility.blog.gov.uk/2016/06/17/colour-contrast-why-does-it-matter/)]
- [ ] Provide `<title>`s that name the site and the specific page [[Read more](https://www.w3.org/TR/WCAG20-TECHS/G88.html)]
- [ ] Make scrollable elements focusable for keyboard users
- [ ] Do not rely on color for differentiation of visual elements
- [ ] Ensure keyboard focus order is logical regarding visual layout
- [ ] Move focus between dialogs and the controls that invoked them
- [ ] Provide status and error messages as WAI-ARIA live regions
- [ ] Provide clear, unambiguous focus styles
- [ ] Ensure states (pressed, expanded, invalid, etc) are communicated to assistive software
- [ ] Match semantics to behavior for assistive technology users
- [ ] Provide a default language and use `lang="[ISO code]"` for subsections in different languages
- [ ] Ensure disabled controls are not focusable
- [ ] Ensure PDF content is accessible (include tags) [[Read more](https://webaim.org/techniques/acrobat/)]
- [ ] Provide a skip link if necessary  [[Read more](https://webaim.org/techniques/skipnav/)]
- [ ] Avoid images of text — text that cannot be translated, selected, or understood by assistive tech
- [ ] Make sure controls within hidden content are not focusable
- [ ] Inform the user when there are important changes to the application state


## Compliance

### Standards

- [ ] Maintain terse HTML, without over-reliance on `<div>` scaffolding [[Read more](http://designingforperformance.com/optimizing-markup-and-styles/#divitis)]
- [ ] Make sure heading levels describe a logical section/subsection structure [[Read more](https://webaim.org/techniques/semanticstructure/)]
- [ ] Only include heading elements where they introduce sections of content
- [ ] Do not recreate supported and expected browser behaviors with bespoke scripts
- [ ] Use data tables (`<table>`) for data only, not visual layout purposes
- [ ] Honour DNT (Do Not Track) header [[Read more](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/DNT)]
- [ ] Make sure all content belongs to a landmark element (`<header>`, `<footer>`, `<nav>`, `<main>`, etc)
- [ ] Do not mark up subheadings/straplines with separate heading elements
- [ ] Provide a print stylesheet (single column, with interactive content hidden)


### Readability

- [ ] Remove potentially insensitive or uninclusive language (use "singular they") [[Read more](http://alexjs.com/)]
- [ ] Underline links — at least in body copy
- [ ] Avoid pure white or pure black shades
- [ ] Label and describe the same things with the same terminology
- [ ] Ensure that content is written as clearly and simply as possible [[Read more](https://www.w3.org/TR/UNDERSTANDING-WCAG20/meaning-supplements.html)]
- [ ] Provide descriptive captions for figures
- [ ] Warn users of links that have unusual behaviors, like linking off-site, or loading a new tab
- [ ] Make content easier to find and improve search results with structured data [[Read more](https://developers.google.com/search/docs/guides/prototype)]
- [ ] Avoid all-caps text [[Read more](https://github.com/humanmade/hm-pattern-library/issues/75)]
- [ ] Use textual labels to make voice activation cues obvious
- [ ] Ensure primary calls to action are easy to recognize and reach


### Other

- [ ] Use relative units (`em`, `rem`, and `ch`), especially for font metrics
- [ ] Use content-based, not device-specific, media queries [[Read more](http://bradfrost.com/blog/post/7-habits-of-highly-effective-media-queries/#content)]
- [ ] Make sure data tables wider than their container can be scrolled horizontally
- [ ] Honour requests to remove animation via the `prefers-reduced-motion` media query
- [ ] Make sure controls do not elicit unexpected or jarring behavior [[Read more](https://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-receive-focus.html)] [[Read more](https://www.w3.org/TR/UNDERSTANDING-WCAG20/consistent-behavior-unpredictable-change.html)]
- [ ] Do not include third parties that compromise user privacy [[Read more](https://css-tricks.com/potential-dangers-of-third-party-javascript/)]
- [ ] Provide large touch "targets" for interactive elements [[Read more](http://www.bbc.co.uk/guidelines/futuremedia/accessibility/mobile/design/touch-target-size)]
- [ ] Use the same design patterns to solve the same problems
- [ ] Do not hijack standard scrolling behavior
- [ ] Make controls look like controls; give them strong perceived affordance
- [ ] Provide a `manifest.json` file for identifiable homescreen entries
- [ ] Avoid time constraints where possible; provide a clear warning and option to extend where not possible
- [ ] Do not instate "infinite scroll" by default; provide buttons to load more items
- [ ] Use well-established, therefore recognizable, icons and symbols
- [ ] Instead of obstructing users with CAPTCHAs, use honeypots [[Read more](https://en.wikipedia.org/wiki/Honeypot_(computing))]
- [ ] Begin long, multi-section documents with a table of contents
- [ ] Don't make users perform actions to reveal content unless completely necessary
- [ ] Break up long and complex forms into discrete sections and/or screens
- [ ] Make forms as short as possible; offer shortcuts like autocompleting the address using the postcode
