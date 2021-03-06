tex2svg
===
[![NPM version][npm-image]][npm-url] [![Build Status][build-image]][build-url] [![Coverage Status][coverage-image]][coverage-url] [![Dependencies][dependencies-image]][dependencies-url]

> Convert a [TeX][tex] or [LaTeX][latex] `string` to an SVG.

<a target="_blank" rel="nofollow" href="https://app.codesponsor.io/link/2GH3ESgBANYoWNMCAicW2LQk/kgryte/tex-equation-to-svg"><img alt="Sponsor" width="888" height="68" src="https://app.codesponsor.io/embed/2GH3ESgBANYoWNMCAicW2LQk/kgryte/tex-equation-to-svg.svg"/></a>


## Installation

``` bash
$ npm install tex-equation-to-svg
```


## Usage

``` javascript
var tex2svg = require( 'tex-equation-to-svg' );
```

<a name="tex2svg"></a>
#### tex2svg( str[, options], clbk )

Converts a [TeX][tex] or [LaTeX][latex] `string` to an SVG.

``` javascript
var eqn = 'y = mx + b';

tex2svg( eqn, clbk );

function clbk( error, svg ) {
	if ( error ) {
		throw error;
	}
	console.log( svg );
	/*
		'<svg xmlns:xlink="http://www.w3.org/1999/xlink" width="11.462ex" height="2.509ex" style="vertical-align: -0.671ex;" viewBox="0 -791.3 4935 1080.4" role="math" focusable="false" xmlns="http://www.w3.org/2000/svg" aria-labelledby="MathJax-SVG-1-Title MathJax-SVG-1-Desc">
		<title id="MathJax-SVG-1-Title">Equation</title>
		<desc id="MathJax-SVG-1-Desc">y equals m x plus b</desc>
		<defs aria-hidden="true">
		<path stroke-width="1" id="E1-MJMATHI-79" d="M21 287Q21 301 36 335T84 406T158 442Q199 442 224 419T250 355Q248 336 247 334Q247 331 231 288T198 191T182 105Q182 62 196 45T238 27Q261 27 281 38T312 61T339 94Q339 95 344 114T358 173T377 247Q415 397 419 404Q432 431 462 431Q475 431 483 424T494 412T496 403Q496 390 447 193T391 -23Q363 -106 294 -155T156 -205Q111 -205 77 -183T43 -117Q43 -95 50 -80T69 -58T89 -48T106 -45Q150 -45 150 -87Q150 -107 138 -122T115 -142T102 -147L99 -148Q101 -153 118 -160T152 -167H160Q177 -167 186 -165Q219 -156 247 -127T290 -65T313 -9T321 21L315 17Q309 13 296 6T270 -6Q250 -11 231 -11Q185 -11 150 11T104 82Q103 89 103 113Q103 170 138 262T173 379Q173 380 173 381Q173 390 173 393T169 400T158 404H154Q131 404 112 385T82 344T65 302T57 280Q55 278 41 278H27Q21 284 21 287Z"></path>
		<path stroke-width="1" id="E1-MJMAIN-3D" d="M56 347Q56 360 70 367H707Q722 359 722 347Q722 336 708 328L390 327H72Q56 332 56 347ZM56 153Q56 168 72 173H708Q722 163 722 153Q722 140 707 133H70Q56 140 56 153Z"></path>
		<path stroke-width="1" id="E1-MJMATHI-6D" d="M21 287Q22 293 24 303T36 341T56 388T88 425T132 442T175 435T205 417T221 395T229 376L231 369Q231 367 232 367L243 378Q303 442 384 442Q401 442 415 440T441 433T460 423T475 411T485 398T493 385T497 373T500 364T502 357L510 367Q573 442 659 442Q713 442 746 415T780 336Q780 285 742 178T704 50Q705 36 709 31T724 26Q752 26 776 56T815 138Q818 149 821 151T837 153Q857 153 857 145Q857 144 853 130Q845 101 831 73T785 17T716 -10Q669 -10 648 17T627 73Q627 92 663 193T700 345Q700 404 656 404H651Q565 404 506 303L499 291L466 157Q433 26 428 16Q415 -11 385 -11Q372 -11 364 -4T353 8T350 18Q350 29 384 161L420 307Q423 322 423 345Q423 404 379 404H374Q288 404 229 303L222 291L189 157Q156 26 151 16Q138 -11 108 -11Q95 -11 87 -5T76 7T74 17Q74 30 112 181Q151 335 151 342Q154 357 154 369Q154 405 129 405Q107 405 92 377T69 316T57 280Q55 278 41 278H27Q21 284 21 287Z"></path>
		<path stroke-width="1" id="E1-MJMATHI-78" d="M52 289Q59 331 106 386T222 442Q257 442 286 424T329 379Q371 442 430 442Q467 442 494 420T522 361Q522 332 508 314T481 292T458 288Q439 288 427 299T415 328Q415 374 465 391Q454 404 425 404Q412 404 406 402Q368 386 350 336Q290 115 290 78Q290 50 306 38T341 26Q378 26 414 59T463 140Q466 150 469 151T485 153H489Q504 153 504 145Q504 144 502 134Q486 77 440 33T333 -11Q263 -11 227 52Q186 -10 133 -10H127Q78 -10 57 16T35 71Q35 103 54 123T99 143Q142 143 142 101Q142 81 130 66T107 46T94 41L91 40Q91 39 97 36T113 29T132 26Q168 26 194 71Q203 87 217 139T245 247T261 313Q266 340 266 352Q266 380 251 392T217 404Q177 404 142 372T93 290Q91 281 88 280T72 278H58Q52 284 52 289Z"></path>
		<path stroke-width="1" id="E1-MJMAIN-2B" d="M56 237T56 250T70 270H369V420L370 570Q380 583 389 583Q402 583 409 568V270H707Q722 262 722 250T707 230H409V-68Q401 -82 391 -82H389H387Q375 -82 369 -68V230H70Q56 237 56 250Z"></path>
		<path stroke-width="1" id="E1-MJMATHI-62" d="M73 647Q73 657 77 670T89 683Q90 683 161 688T234 694Q246 694 246 685T212 542Q204 508 195 472T180 418L176 399Q176 396 182 402Q231 442 283 442Q345 442 383 396T422 280Q422 169 343 79T173 -11Q123 -11 82 27T40 150V159Q40 180 48 217T97 414Q147 611 147 623T109 637Q104 637 101 637H96Q86 637 83 637T76 640T73 647ZM336 325V331Q336 405 275 405Q258 405 240 397T207 376T181 352T163 330L157 322L136 236Q114 150 114 114Q114 66 138 42Q154 26 178 26Q211 26 245 58Q270 81 285 114T318 219Q336 291 336 325Z"></path>
		</defs>
		<g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)" aria-hidden="true">
		 <use xlink:href="#E1-MJMATHI-79" x="0" y="0"></use>
		 <use xlink:href="#E1-MJMAIN-3D" x="775" y="0"></use>
		 <use xlink:href="#E1-MJMATHI-6D" x="1831" y="0"></use>
		 <use xlink:href="#E1-MJMATHI-78" x="2710" y="0"></use>
		 <use xlink:href="#E1-MJMAIN-2B" x="3504" y="0"></use>
		 <use xlink:href="#E1-MJMATHI-62" x="4505" y="0"></use>
		</g>
		</svg>'
	*/
}
```

The `function` accepts the following `options`:
*	__width__: container width in `ex` (used for linebreaking and tags). Default: `100`.
*	__ex__: `ex` size in pixels. Default: `6`.
*	__inline__: `boolean` indicating whether to format an input `string` as an inline equation. Default: `false`.
*	__linebreaks__: `boolean` indicating whether to perform linebreaking. Default: `true`.

By default, the `function` formats an input `string` as a displayed equation. To format the `string` as a text (inline) equation, set the `inline` option to `true`.

``` javascript
var eqn = 'y = mx + b';

var opts = {
	'inline': true
};

tex2svg( eqn, opts, clbk );
```


#### tex2svg.factory( options, clbk )

Creates a reusable `function`.

``` javascript
var opts = {
	'inline': true
};

var convert = tex2svg.factory( opts, clbk );

convert( 'y = mx + b' );
convert( 'z = \\frac{1}{2}' );
convert( 'w = \\sum_{i=0}^{n} x_i' );
// ...
```

The factory method accepts the same `options` as [`tex2svg()`](#tex2svg).


## Notes

*	All [TeX][tex] and [LaTeX][latex] commands should be escaped.
	
	``` javascript
	// Not escaped:
	var eqn = 'x = \frac{1}{2}';

	// Escaped:
	eqn = 'x = \\frac{1}{2}';
	```


## Examples

``` javascript
var tex2svg = require( 'tex-equation-to-svg' );

var eqn = '\\operatorname{erf}(x) = \\frac{2}{\\sqrt\\pi}\\int_0^x e^{-t^2}\\,\\mathrm dt.';

tex2svg( eqn, done );

function done( error, svg ) {
	if ( error ) {
		throw error;
	}
	console.log( svg );
	// returns '<string>'
}
```

To run the example code from the top-level application directory,

``` bash
$ node ./examples/index.js
```


---
## CLI

### Installation

To use the module as a general utility, install the module globally

``` bash
$ npm install -g tex-equation-to-svg
```


### Usage

``` bash
Usage: tex2svg [options] equation

Options:

  -h,  --help               Print this message.
  -V,  --version            Print the package version.
       --width width        Container width in ex. Default: 100.
       --ex ex              ex size in pixels. Default: 6.
       --inline             Format input equation as inline TeX.
       --no-linebreaks      Disable linebreaking.
```


### Examples

``` bash
$ tex2svg '\operatorname{erf}(x) = \frac{2}{\sqrt\pi}\int_0^x e^{-t^2}\,\mathrm dt.'
# => <svg xmlns:xlink="http://www.w3.org/1999/xlink" width="24.594ex" ...
```

For local installations, modify the command to point to the local installation directory; e.g., 

``` bash
$ ./node_modules/.bin/tex2svg '\operatorname{erf}(x) = \frac{2}{\sqrt\pi}\int_0^x e^{-t^2}\,\mathrm dt.'
# => <svg xmlns:xlink="http://www.w3.org/1999/xlink" width="24.594ex" ...
```

Or, if you have cloned this repository and run `npm install`, modify the command to point to the executable; e.g., 

``` bash
$ node ./bin/cli '\operatorname{erf}(x) = \frac{2}{\sqrt\pi}\int_0^x e^{-t^2}\,\mathrm dt.'
# => <svg xmlns:xlink="http://www.w3.org/1999/xlink" width="24.594ex" ...
```


---
## Tests

### Unit

This repository uses [tape][tape] for unit tests. To run the tests, execute the following command in the top-level application directory:

``` bash
$ make test
```

All new feature development should have corresponding unit tests to validate correct functionality.


### Test Coverage

This repository uses [Istanbul][istanbul] as its code coverage tool. To generate a test coverage report, execute the following command in the top-level application directory:

``` bash
$ make test-cov
```

Istanbul creates a `./reports/coverage` directory. To access an HTML version of the report,

``` bash
$ make view-cov
```


---
## License

[MIT license](http://opensource.org/licenses/MIT).


## Copyright

Copyright &copy; 2016. Athan Reines.


[npm-image]: http://img.shields.io/npm/v/tex-equation-to-svg.svg
[npm-url]: https://npmjs.org/package/tex-equation-to-svg

[build-image]: http://img.shields.io/travis/kgryte/tex-equation-to-svg/master.svg
[build-url]: https://travis-ci.org/kgryte/tex-equation-to-svg

[coverage-image]: https://img.shields.io/codecov/c/github/kgryte/tex-equation-to-svg/master.svg
[coverage-url]: https://codecov.io/github/kgryte/tex-equation-to-svg?branch=master

[dependencies-image]: http://img.shields.io/david/kgryte/tex-equation-to-svg.svg
[dependencies-url]: https://david-dm.org/kgryte/tex-equation-to-svg

[dev-dependencies-image]: http://img.shields.io/david/dev/kgryte/tex-equation-to-svg.svg
[dev-dependencies-url]: https://david-dm.org/dev/kgryte/tex-equation-to-svg

[github-issues-image]: http://img.shields.io/github/issues/kgryte/tex-equation-to-svg.svg
[github-issues-url]: https://github.com/kgryte/tex-equation-to-svg/issues

[tape]: https://github.com/substack/tape
[istanbul]: https://github.com/gotwarlost/istanbul

[tex]: https://en.wikipedia.org/wiki/TeX
[latex]: https://en.wikipedia.org/wiki/LaTeX
