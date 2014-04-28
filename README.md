# normalize.scss

normalize.scss is a configurable version of [normalize.css](http://necolas.github.io/normalize.css/), using CSS Sass preprocessor.

[Version FR](https://github.com/Effeilo/normalize.scss/blob/master/README-FR.md)

1. [Install normalize.scss](#install-normalizescss)
2. [Configure normalize.scss](#configure-normalizescss) 
  * [options](#options)
  * [base](#base)
  * [html5 display definitions](#html5-display-definitions)
  * [links](#links)
  * [text level semantics](#text-level-semantics)
  * [embedded content](#embedded-content)
  * [grouping content](#grouping-content)
  * [forms](#forms)
  * [tables](#tables)

## Install normalize.scss

- Download the project.
- Copy the files to where you put your CSS files.
- Call normalize.css in your html file :

```html
<link rel="stylesheet" href="normalize.css">
```

## Configure normalize.scss

The configuration happens in the file normalize.scss.

```scss
$normalize-settings: (

	...

);
``` 

### options

```scss
"options": (
	"explanations comments":          true  // true;false
),
```

##### `eplanations comments`

- `true` : displays explanatory comments
- `false` : hide explanatory comments

### Base

```scss
"base": (
	"html":                           true, // true;false
	"reset margin":                   "body"// false;"list of tags, in quotation marks, separated by commas"
),
```

##### `html`

- `true` : displays the code
- `false` : hide the code

```css
/**
 * 1. Set default font family to sans-serif.
 * 2. Prevent iOS text size adjust after orientation change, without disabling
 *    user zoom.
 */
 
html {
	font-family: sans-serif; /* 1 */
	-ms-text-size-adjust: 100%; /* 2 */
	-webkit-text-size-adjust: 100%; /* 2 */
}
```

##### `reset margin`

- `"list of tags, in quotation marks, separated by commas"` : displays the code
- `false` : hide the code

```scss
"reset margin":                   "body, div"
```
```css
/**
 * Remove default margin.
 */
 
body, div {
	margin: 0;
}
```

### html5 display definitions

```scss
"html5 display definitions": (
	"block":                          true, // true;false
	"inline block":                   true, // true;false
	"audio":                          true, // true;false
	"hidden template":                true  // true;false
),
```
- `true` : displays the code
- `false` : hide le code

##### `block`

```css
/**
 * Correct `block` display not defined for any HTML5 element in IE 8/9.
 * Correct `block` display not defined for `details` or `summary` in IE 10/11 and Firefox.
 * Correct `block` display not defined for `main` in IE 11.
 */

article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
nav,
section,
summary {
	display: block;
}
```

##### `inline block`

```css
/**
 * 1. Correct `inline-block` display not defined in IE 8/9.
 * 2. Normalize vertical alignment of `progress` in Chrome, Firefox, and Opera.
 */

audio,
canvas,
progress,
video {
	display: inline-block; /* 1 */
	vertical-align: baseline; /* 2 */
}
```

##### `audio`

```css
/**
 * Prevent modern browsers from displaying `audio` without controls.
 * Remove excess height in iOS 5 devices.
 */

audio:not([controls]) {
	display: none;
	height: 0;
}
```

##### `hidden template`

```css
/**
 * Address `[hidden]` styling not present in IE 8/9/10.
 * Hide the `template` element in IE 8/9/11, Safari, and Firefox < 22.
 */

[hidden],
template {
  display: none;
}

```

### links

```scss
"links": (
	"background":                     true, // true;false
	"outline":                        true  // true;false
),
```
- `true` : displays the code
- `false` : hide le code

##### `background`

```css
/**
 * Remove the gray background color from active links in IE 10.
 */

a {
	background: transparent;
}
```

##### `outline`

```css
/**
 * Improve readability when focused and also mouse hovered in all browsers.
 */

a:active,
a:hover {
	outline: 0;
}
```

### text level semantics

```scss
"text level semantics": (
	"abbr":                           true, // true;false
	"b strong":                       true, // true;false
	"dfn":                            true, // true;false
	"h1":                             true, // true;false
	"mark":                           true, // true;false
	"small":                          true, // true;false
	"sub sup":                        true  // true;false
),
```
- `true` : displays the code
- `false` : hide le code

##### `abbr`

```css
/**
 * Address styling not present in IE 8/9/10/11, Safari, and Chrome.
 */

abbr[title] {
	border-bottom: 1px dotted;
}
```

##### `b strong`

```css
/**
 * Address style set to `bolder` in Firefox 4+, Safari, and Chrome.
 */

b,
strong {
	font-weight: bold;
}
```

##### `dfn`

```css
/**
 * Address styling not present in Safari and Chrome.
 */

dfn {
	font-style: italic;
}
```

##### `h1`

```css
/**
 * Address variable `h1` font-size and margin within `section` and `article`
 * contexts in Firefox 4+, Safari, and Chrome.
 */

h1 {
	font-size: 2em;
	margin: 0.67em 0;
}
```

##### `mark`

```css
/**
 * Address styling not present in IE 8/9.
 */

mark {
	background: #ff0;
	color: #000;
}
```

##### `small`

```css
/**
 * Address inconsistent and variable font size in all browsers.
 */

small {
	font-size: 80%;
}
```

##### `sub sup`

```css
/**
 * Prevent `sub` and `sup` affecting `line-height` in all browsers.
 */

sub,
sup {
	font-size: 75%;
	line-height: 0;
	position: relative;
	vertical-align: baseline;
}

sup {
	top: -0.5em;
}

sub {
	bottom: -0.25em;
}
```

### embedded content

```scss
"embedded content": (
	"img":                            true, // true;false
	"svg":                            true  // true;false
),
```
- `true` : displays the code
- `false` : hide le code

##### `img`

```css
/**
 * Remove border when inside `a` element in IE 8/9/10.
 */

img {
	border: 0;
}
```

##### `svg`

```css
/**
 * Correct overflow not hidden in IE 9/10/11.
 */

svg:not(:root) {
	overflow: hidden;
}
```

### grouping content

```scss
"grouping content": (
	"figure":                         true, // true;false
	"hr":                             true, // true;false
	"pre":                            true, // true;false
	"code kbd pre samp":              true  // true;false
),
```
- `true` : displays the code
- `false` : hide le code

##### `figure`

```css
/**
 * Address margin not present in IE 8/9 and Safari.
 */

figure {
	margin: 1em 40px;
}
```

##### `hr`

```css
/**
 * Address differences between Firefox and other browsers.
 */

hr {
	-moz-box-sizing: content-box;
	box-sizing: content-box;
	height: 0;
}
```

##### `pre`

```css
/**
 * Contain overflow in all browsers.
 */

pre {
	overflow: auto;
}
```

##### `code kbd pre samp`

```css
/**
 * Address odd `em`-unit font size rendering in all browsers.
 */

code,
kbd,
pre,
samp {
	font-family: monospace, monospace;
	font-size: 1em;
}
```

### forms

```scss
"forms": (
	"form elements reset":            true, // true;false
	"button overflow":                true, // true;false
	"button select text transform":   true, // true;false
	"button appearance":              true, // true;false
	"button input disabled":          true, // true;false
	"button input focus inner":       true, // true;false
	"input line height":              true, // true;false
	"input checkbox radio":           true, // true;false
	"input number":                   true, // true;false
	"input search":                   true, // true;false
	"fieldset":                       true, // true;false
	"legend":                         true, // true;false
	"textarea":                       true, // true;false 
	"optgroup":                       true  // true;false 
),
```
- `true` : displays the code
- `false` : hide le code

##### `form elements reset`

```css
/**
 * 1. Correct color not being inherited.
 *    Known issue: affects color of disabled elements.
 * 2. Correct font properties not being inherited.
 * 3. Address margins set differently in Firefox 4+, Safari, and Chrome.
 */

button,
input,
optgroup,
select,
textarea {
	color: inherit; /* 1 */
	font: inherit; /* 2 */
	margin: 0; /* 3 */
}
```

##### `button overflow`

```css
/**
 * Address `overflow` set to `hidden` in IE 8/9/10/11.
 */

button {
	overflow: visible;
}
```

##### `button select text transform`

```css
/**
 * Address inconsistent `text-transform` inheritance for `button` and `select`.
 * All other form control elements do not inherit `text-transform` values.
 * Correct `button` style inheritance in Firefox, IE 8/9/10/11, and Opera.
 * Correct `select` style inheritance in Firefox.
 */

button,
select {
	text-transform: none;
}
```

##### `button appearance`

```css
/**
 * 1. Avoid the WebKit bug in Android 4.0.* where (2) destroys native `audio`
 *    and `video` controls.
 * 2. Correct inability to style clickable `input` types in iOS.
 * 3. Improve usability and consistency of cursor style between image-type
 *    `input` and others.
 */

button,
html input[type="button"],
input[type="reset"],
input[type="submit"] { /* 1 */
	-webkit-appearance: button; /* 2 */
	cursor: pointer; /* 3 */
}
```

##### `button input disabled`

```css
/**
 * Re-set default cursor for disabled elements.
 */

button[disabled],
html input[disabled] {
	cursor: default;
}
```

##### `button input focus inner`

```css
/**
 * Remove inner padding and border in Firefox 4+.
 */

button::-moz-focus-inner,
input::-moz-focus-inner {
	border: 0;
	padding: 0;
}
```

##### `input line height`

```css
/**
 * Address Firefox 4+ setting `line-height` on `input` using `!important` in
 * the UA stylesheet.
 */

input {
	line-height: normal;
}
```

##### `input checkbox radio`

```css
/**
 * It's recommended that you don't attempt to style these elements.
 * Firefox's implementation doesn't respect box-sizing, padding, or width.
 *
 * 1. Address box sizing set to `content-box` in IE 8/9/10.
 * 2. Remove excess padding in IE 8/9/10.
 */

input[type="checkbox"],
input[type="radio"] {
	box-sizing: border-box; /* 1 */
	padding: 0; /* 2 */
}
```

##### `input number`

```css
/**
 * Fix the cursor style for Chrome's increment/decrement buttons. For certain
 * `font-size` values of the `input`, it causes the cursor style of the
 * decrement button to change from `default` to `text`.
 */

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
	height: auto;
}
```

##### `input search`

```css
/**
 * 1. Address `appearance` set to `searchfield` in Safari and Chrome.
 * 2. Address `box-sizing` set to `border-box` in Safari and Chrome
 *    (include `-moz` to future-proof).
 */

input[type="search"] {
	-webkit-appearance: textfield; /* 1 */
	-moz-box-sizing: content-box;
	-webkit-box-sizing: content-box; /* 2 */
	box-sizing: content-box;
}

/**
 * Remove inner padding and search cancel button in Safari and Chrome on OS X.
 * Safari (but not Chrome) clips the cancel button when the search input has
 * padding (and `textfield` appearance).
 */

input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
	-webkit-appearance: none;
}
```

##### `fieldset`

```css
/**
 * Define consistent border, margin, and padding.
 */

fieldset {
	border: 1px solid #c0c0c0;
	margin: 0 2px;
	padding: 0.35em 0.625em 0.75em;
}
```

##### `legend`

```css
/**
 * 1. Correct `color` not being inherited in IE 8/9/10/11.
 * 2. Remove padding so people aren't caught out if they zero out fieldsets.
 */

legend {
	border: 0; /* 1 */
	padding: 0; /* 2 */
}
```

##### `textarea`

```css
/**
 * Remove default vertical scrollbar in IE 8/9/10/11.
 */

textarea {
	overflow: auto;
}
```

##### `optgroup`

```css
/**
 * Don't inherit the `font-weight` (applied by a rule above).
 * NOTE: the default cannot safely be changed in Chrome and Safari on OS X.
 */

optgroup {
	font-weight: bold;
}
```

### tables

```scss
"tables": (
	"table":                          true, // true;false
	"td th":                          true  // true;false
)
```
- `true` : displays the code
- `false` : hide le code

##### `table`

```css
/**
 * Remove most spacing between table cells.
 */

table {
	border-collapse: collapse;
	border-spacing: 0;
}
```

##### `td th`

```css
td,
th {
	padding: 0;
}
```
