# annie

A tiny (675 bytes gzipped) library for authoring cross-browser animations.

## huh?

Annie returns the following information:

```js
{
	ie: Number|false				// internet explorer version (or false)
	performance: Boolean			// browser supports window.performance
	vendor: String					// webkit, moz, ie, or o
	requestAnimationFrame: Function	// requestAnimationFrame, polyfilled if necessary
	cancelAnimationFrame: Function	// cancelAnimationFrame, polyfilled if necessary
	transform: String|undefined		// CSS transform property, if supported
	supports3d: Boolean				// Whether or not browser supports 3D CSS transforms
}
```

## Sample output

| browser				| platform 	| vendor | ie		| performance		| transform				| supports3d	|
|-----------------------|-----------|--------|----------|-------------------|-----------------------|---------------|
| chrome 29				| osx		| Webkit | false	| true				| WebkitTransform		| true			|
| firefox 23			| osx		| Moz	 | false	| true				| MozTransform			| true			|
| opera 16				| osx		| Webkit | false	| true				| WebkitTransform		| true			|
| safari 6				| osx		| Webkit | false	| false				| WebkitTransform		| true			|
| safari 6				| ios		| Webkit | false	| false				| WebkitTransform		| true			|
| safari 6				| ios		| Webkit | false	| false				| WebkitTransform		| true			|
| internet explorer 10	| windows	| ms	 | 10		| true				| msTransform			| true			|



## why not modernizr?

Annie:

- contains an efficiently authored subset of Modernizr's functionality
- is geared towards animation and DOM effects

Modernizr:

- is a hefty ~15kb, big for the functionality it offers
- is overkill for most projects