# annie

A tiny CSS/animation library for authoring cross-browser code.

## huh?

Annie returns the following information:

```js
{
	ie: Number|false				// internet explorer version (or false)
	performance: Boolean			// browser supports window.performance
	vendor: String					// webkit, moz, ie, or o
	requestAnimationFrame: Function
	cancelAnimationFrame: Function
	transform: String|Undefined		// CSS transform property, if supported
	supports3d: Boolean				// Whether or not browser supports 3D CSS transforms
}
```

## why not modernizr?

Annie:

- ... contains an efficiently authored subset of Modernizr's functionality
- ... is geared towards animation and DOM effects rather than a do-it-all approach

Modernizr:

- ... is a hefty ~15kb, big for the functionality it offers
- ... is overkill for most projects