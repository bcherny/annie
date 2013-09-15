# annie

A super tiny library for authoring cross-browser animations.

## huh?

Annie returns the following information:

```js
> annie
{
	ie: Number|false				// internet explorer version (or false)
	vendor: String					// webkit, moz, ie, or o
	requestAnimationFrame: Function	// requestAnimationFrame, polyfilled if necessary
	cancelAnimationFrame: Function	// cancelAnimationFrame, polyfilled if necessary
	transform: String|undefined		// CSS transform property, if supported
	3d: Boolean						// Whether or not browser supports 3D CSS transforms
	performance: Boolean			// browser supports window.performance
}
```

## sample output

### modern browsers
| browser				| platform 	| vendor	| ie		| performance		| transform			| 3d			|
|-----------------------|-----------|-----------|-----------|-------------------|-------------------|---------------|
| chrome 29				| osx		| `Webkit`	| `false`	| `true`			| `WebkitTransform`	| `true`		|
| firefox 23			| osx		| `Moz`	 	| `false`	| `true`			| `MozTransform`	| `true`		|
| internet explorer 10	| windows	| `ms`		| `10`		| `true`			| `msTransform`		| `true`		|
| opera 16				| osx		| `Webkit`	| `false`	| `true`			| `WebkitTransform`	| `true`		|
| safari 6				| ios		| `Webkit`	| `false`	| `false`			| `WebkitTransform`	| `true`		|
| safari 6				| ios		| `Webkit`	| `false`	| `false`			| `WebkitTransform`	| `true`		|
| safari 6				| osx		| `Webkit`	| `false`	| `false`			| `WebkitTransform`	| `true`		|

### legacy browsers
| browser				| platform 	| vendor	| ie		| performance		| transform			| 3d			|
|-----------------------|-----------|-----------|-----------|-------------------|-------------------|---------------|
| firefox 12			| windows	| `Moz`		| `false`	| `false`			| `MozTransform`	| `true`		|
| firefox 10			| windows	| `Moz`		| `false`	| `false`			| `MozTransform`	| `true`		|
| firefox 8				| windows	| `Moz`		| `false`	| `false`			| `MozTransform`	| `false`		|
| internet explorer 9	| windows	| `ms`		| `9`		| `false`			| `msTransform`		| `false`		|
| internet explorer 8	| windows	| `ms`		| `8`		| `false`			| `undefined`		| `false`		|
| internet explorer 7	| windows	| `ms`		| `7`		| `false`			| `undefined`		| `false`		|
| opera 11				| windows	| `O`		| `false`	| `false`			| `OTransform`		| `false`		|
| safari 5				| windows	| `Webkit`	| `false`	| `false`			| `WebkitTransform`	| `true`		|

## why not modernizr?

Annie:

- contains an efficiently authored subset of Modernizr's functionality
- is geared towards animation and DOM effects

Modernizr:

- is a hefty ~15kb, big for the functionality it offers
- is overkill for most projects