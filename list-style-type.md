#list-style-type

The `list-style-type` property identifies a tag's list-item marker. This property only applies to elements with a `display` value of `list-item`, and it's usually applied to the &lt;ul&gt;, &lt;ol&gt;, and &lt;li&gt; tags.

## Syntax

Syntax: `list-style-type: value;`

## Property Values

The `list-style-type` property can be divided into global, unordered and ordered values. Below is a list of values supported in all modern browsers. See [Browser Support](#Browser-Support) for a full list of values.

### Global
- **inherit**: Uses the `list-style-type` property of its parent element.
 
### Unorderd Lists Values

- **circle**: An empty circle marker (○).
- **disc**: A filled circle marker and is the default for `<ul>`.(●)
- **none**: No marker is shown
- **square**: A filled square marker(■).

### Ordered Lists Values

- **armenian**: Traditional uppercase Armenian numbering (    &#1329;, &#1330;, &#1331;, etc.).
- **decimal**: A number beginning with 1. This is the default for `<ol>`. 
- **decimal-leading-zero**: A leading zero fills in the space for decimal numbers 1–9 (01, 02, 03, ..., 98, 99, etc.).
- **georgian**: Traditional lowercase Georgian numbering (&#4304;, &#4305;, &#4306;, etc.).
- **lower-alpha**: Lowercase ascii letters (a, b, c, ... z).
- **lower-greek**: Lowercase classical Greek alpha, beta, gamma, ... (α, β, γ, etc.).
- **lower-latin**: Lowercase ascii letters (a, b, c, ... z).
- **lower-roman**: Lowercase Roman numerals (i, ii, iii, iv, v, etc.).
- **upper-alpha**: Uppercase ascii letters (A, B, C, ... Z). 
- **upper-latin**: Uppercase ascii letters (A, B, C, ... Z).
- **upper-roman**: Uppercase Roman numerals (I, II, III, IV, V, etc.).

## Usage
### Example 1

In this example, we create an ordered list with `lower-roman` list-item markers.

```
 <!-- HTML -->
 <ol>
	<li>Item 1</li>
	<li>Item 2</li>
	<li>Item 3</li>
	<li>Item 4</li>
 </ol>
 
 /* CSS */
 ol {
 	list-style-type: lower-roman;
 }
```

### Example 2

In this example we see an unordered list used to create a vertical navigation, it has a `square` list-item marker.

```
 <!-- HTML -->
 <ul>
 	<li><a href="#">Home</a></li>
 	<li><a href="#">About</a></li>
 	<li><a href="#">Blog</a></li>
 	<li><a href="#">Events</a></li>
 	<li><a href="#">Contact</a></li>
 </ul>
 
 /* CSS */
 ul {
 	list-style-type: square;
 }
 ```

### Example 3

In this example, we see a nested ordered list with a `circle` list-item marker and an ordered list with a `decimal` list-item marker.

```
 <!-- HTML -->
 <ol>
 	<li>Item 1
 		<ul>
 			<li>Text</li>
 			<li>Text</li>
 		</ul>
 	</li>
 	<li>Item 2
 		<ul>
 			<li>Text</li>
 			<li>Text</li>
 		</ul>
 	</li>
 	<li>Item 3
 		<ul>
 			<li>Text</li>
 			<li>Text</li>
 		</ul>
 	</li>
 	<li>Item 4
 		<ul>
 			<li>Text</li>
 			<li>Text</li>
 		</ul>
 	</li>
 </ol>

 /* CSS */
 ol li{
 	list-style-type: upper-roman;
 }

 ul li {
 	list-style-type: circle;
 }
```

## Browser Support 

This table contains the first browser version that fully supports the `list-style-type` property.

|Chrome | IE / Edge | Firefox | Safari | Opera |
|:------|:------------------------:|:-------:|:-------|:------|
| 1.0 | 4.0 | 1.0| 1.0 | 3.5 |

This table shows which browsers support each value.

| Feature | Chrome | Firefox (Gecko) | IE / Edge  | Opera | Safari (WebKit)|
|:------|:---------|:----------|:--------|:-------|:------|
| none, disc, circle, square, decimal, lower-alpha, upper-alpha, lower-roman, upper-roman | 1.0 | 1.0 (1.0) | 4.0 | 3.5 | 1.0 (85) |
| lower-latin, upper-latin, lower-greek, armenian, georgian | 1.0 | 1.0 (1.0) | 8.0 | 6.0 | 1.0 (85) |
| decimal-leading-zero | 1.0 | 1.0 (1.0) | 8.0 | 8.0 | 1.0 (85) |
| hebrew, cjk-ideographic, hiragana, hiragana-iroha, katakana, katakana-iroha (experimental and should not be used in production code) | 1.0 | 1.0 (1.0) | Not supported | 7.0 (but displays decimal numbers only) 15.0 | 1.0-1.2 (85-125)|
| japanese-formal, japanese-informal, simp-chinese-formal, trad-chinese-formal, simp-chinese-informal, trad-chinese-informal (experimental and should not be used in production code) | Not supported | 1.0 (1.7 or earlier) -moz 28.0 (28.0) | Not supported | Not supported | Not supported |
| korean-hangul-formal, korean-hanja-informal, korean-hanja-formal, cjk-decimal (experimental and should not be used in production code) | Not supported | 28.0 (28.0) | Not supported | Not supported | Not supported |
| ethiopic-numeric, persian, arabic-indic, devanagari, bengali, gurmukhi, gujarati, oriya, tamil, telugu, kannada, malayalam, thai, lao, myanmar, khmer, cjk-heavenly-stem, cjk-earthly-branch (experimental and should not be used in production code) | Not supported | 1.0 (1.7 or earlier) -moz 33.0 (33.0) | Not supported | Not supported |Not supported|
| disclosure-open, disclosure-closed, mongolian (experimental and should not be used in production code) | Not supported | 33.0 (33.0) | Not supported | Not supported | Not supported |
| &lt;string&gt; | Not supported | 39.0 (39.0) | Not supported | Not supported | Not supported |

## Special Notes

### Change the color of a list-item marker

The list-item marker inherits the color of the element it's applied to. To make this marker a different color, without using an image, nest a &lt;span&gt; tag within each &lt;li&gt;. After adding the &lt;span&gt; tag, set the preferred color of each &lt;li&gt; and &lt;span&gt;. You do not need to use a &lt;span&gt; tag if you have a nested link because you can style each link. 

```
 <!-- HTML -->
 <ul>
 	<li><span>Item 1</span></li>
 	<li><span>Item 2</span></li>
 	<li><span>Item 3</span></li>
 </ul>

 /* CSS *
 li {
 	color: red; /* BULLIT COLOR */
 }
 li span {
 	color: blue; /* TEXT COLOR */
 }
```

