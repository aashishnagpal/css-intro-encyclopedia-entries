# Border: `border-right`

*`border-right` is one of the many CSS properties that can be set to specify the border style, color and width on an element.*

`border-right` can be regarded both a shorthand and a longhand notation depending on what is the context. It is considered a longhand notation and proves very useful if one has to set just the right-hand border on an element. On the other hand, it is a shorthand notation to specify border-right-width, border-right-style and border-right-color all together in just one property.

## Syntax

`border-right` syntax is below:

```css
border-right: <border-width> <border-style> <color>

border-right: inherit /*border properties are not inherited by default*/
```

### Values
The border-right property can contain up to three components:

#### border-width
This takes a numeric value with any of the standard length units. The length units can be, for example `px` (pixels), `pt` (points), `em`/`rem` (relative units).

#### border-style
This takes any of the range of style values available to the `border-style` property, which includes **none**, **hidden**, **dotted**, **dashed**, **solid**, **double**, **groove**, **ridge**, **inset**, **outset**. For more details about each, see [Special Notes](#special-notes).

#### color
This can take any valid CSS color as its value. Valid color includes all the 140 predefined color constants, any of the possible HEX or RGB values and even RGBA values (which has a defined transparency of the color).

#### inherit
When we set the value to inherit, the element will inherit the border values set on its parent (or any ancestor, whichever has this property defined for itself; the CSS engine traverses from current element until the topmost parent).


## Examples

### Example 1

A simple, basic `border-right` example

```css
border-right: 1px solid black;
``` 

### Example 2

The three values of the shorthand property can be specified in any order.

```css
border-right: solid 1px black;

border-right: red solid 2px
``` 


### Example 3

Any one or two of the three values of the shorthand property may be omitted.

```css
border-right: 1px black; /*border-style will be none by default*/

border-right: dashed 1px; /*border-color will be currentColor by default*/

border-right: dotted red; /*border-width will be medium by default*/
``` 

### Example 4

A more interesting border example to round things off, showing a basic border being set, and then the right border being overridden
```css
.className {
    border: 1px inset black;
    border-right: 10px inset rgba(234,190,50,0.75);
}
```

## Special Notes

- The three properties, border-right-width, border-right-style and border-right-color together describe the right border of the element(s). The initial values for these three are the same as for the border properties and as follows.

 Initial/Default value for:
 
 -  border-right-width = border-width = medium, which is computed as about 3px in most browsers
 - border-right-style = border-style = none
 - border-right-color = border-color = currentColor (set on body, default black)


- The border-style property specifies what kind of border to display. The following values are allowed:

 - **none** - Defines no border
 - **hidden** - Defines a hidden border
 - **dotted** - Defines a dotted border
 - **dashed** - Defines a dashed border
 - **solid** - Defines a solid border
 - **double** - Defines a double border
 - **groove** - Defines a 3D grooved border. The effect depends on the border-color value
 - **ridge** - Defines a 3D ridged border. The effect depends on the border-color value
 - **inset** - Defines a 3D inset border. The effect depends on the border-color value
 - **outset** - Defines a 3D outset border. The effect depends on the border-color value

- (Source: [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right)) The three values of the shorthand property can be specified in any order, and one or two of them may be omitted.

 As with all shorthand properties, `border-right` always sets the values of all of the properties that it can set, even if they are not specified. It sets those that are not specified to their default values. This means that:

    ```css
    border-right-style: dotted;
    border-right: thick green;
    ```

 is actually the same as
    
    ```css
    border-right-style: dotted;
    border-right: none thick green;
    ```

 and the value of `border-right-style` given before `border-right` is ignored.

 Since the default value of `border-right-style` is **none**, not specifying the `border-style` part of the value means that the property specifies its default value which is *none* and means no border.