# window.innerWidth

The width (in pixels) of the browser window including the vertical scrollbar (if it is rendered).

## Syntax

```javascript

var innerWindowWidth = window.innerWidth;

```

## Value

`innerWindowWidth` above stores the `window.innerWidth` property value.

The `window.innerWidth` property is read only; it has no default value.

## Usage/Examples

```javascript

// This will return the width of the viewport
var innerWindowWidth = window.innerWidth;

```
## Special  Notes

This is a method to determine the width of the currently available content area or viewport and is *not a foolproof way*. There are a lot of cross browser compatibility issues, i.e. what is supported in one browser is not supported in other. The calculation or determination of value is not consistent within the browsers. Some have the vertical scroll bar width included in `window.innerWidth` while some exclude that.

There are also similar values defined by browsers for what was the need of the hour. Some browsers define `clientWidth` over the `window` object to say that `window.innerWidth` includes the vertical scrollbar while `window.clientWidth` does not. Some other browsers have implementation of `clientWidth` but not on `window` object but on `document.documentElement` which is different from the `window` object.

In today's world where Responsive Design is a need due to availability of so many different devices with different screen sizes, being able to properly calculate the width (or height) of the viewport is sometimes critical. Almost all developers have to resort to an algorithm or combination of multiple fallback values to be able to somewhat determine and approximate the available viewport width (or height). Many rely on just the media queries in CSS, while some make use of opinionated CSS libraries like Bootstrap to create a Responsive design.

#### Browser Compatibility

|           Browser             | Chrome |   Firefox (Gecko)    | Internet Explorer | Opera | Safari |
| ----------------------------- | ------ | -------------------- | ----------------- | ----- | ------ |
| Version (including and above) |    1   | 1.0 (1.7 or earlier) |          9        |   9   |   3    |

-

From Firefox 4 to 24, this property was buggy and could give a wrong value before page load on certain circumstances. **It is recommended to always read this value after ensuring that the page and the HTML document has completely loaded.**

IE8 and below do not support this at all.