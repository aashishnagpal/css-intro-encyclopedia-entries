# The &lt;frame&gt; tag

&lt;frame&gt; is an HTML element which defines a particular area within the HTML Document in which another HTML document can be displayed. 

Frames allow you to have multiple sections of the browser window, called frames, each showing their own `.html` file within the frame. This used to be common practice when trying to show separate sections of a site in separate sections of the browser window, such as a header at the top, navigation at the side, and the rest was page content that someone could scroll down without making the header and navigation disappear.

## Attributes

The frame tag has 7 associated attributes.

- **src**: This attribute specifies the HTML document which will be displayed by frame. It is usually a URL to a separate `.htm` or `.html` file.

- **name**: This attribute is used to labeling frames. Without labeling all links will open in the frame that they are in.

- **noresize**: This attribute avoid resizing of frames by users. The frames by default have resizing borders allowing the user to scale and increase or decrease a frame's size.

- **scrolling**: This attribute defines existence of scrollbar. If this attribute is not used, browser put a scrollbar when necessary. There are two choices; "yes" for showing a scrollbar even when it is not necessary and "no" for do not showing a scrollbar even when it is necessary.

- **marginheight**: This attribute defines how tall the margin between frames will be.

- **marginwidth**: This attribute defines how wide the margin between frames will be.

- **frameborder**: This attribute allows you to put borders for frames.

Apart from these attributes, `<frame>` also supports global attributes.

## Usage
Frames are always defined within `<frameset></frameset>`. The frameset defines how the frames will be spread across the page in how many columns and rows.

#### Example 1
Adding a single frame to HTML.
```html
<frameset>
  <frame name="framename" src="sample-frame.html" />
</frameset>
```

#### Example 2
Adding 2 frames aligned horizontally into columns.
```html
<frameset cols="50%,50%">
  <frame name="frame1" src="sample-1.html" />
  <frame name="frame2" src="sample-2.html" />
</frameset>
```

#### Example 3
Adding 2 frames aligned vertically into rows.
```html
<frameset rows="50%,50%">
  <frame name="frame1" src="sample-1.html" />
  <frame name="frame2" src="sample-2.html" />
</frameset>
```

#### Example 4
Using other attributes.
```html
<frameset cols="50%,50%">
  <frame name="frame1" src="sample-1.html" scrolling="no" frameborder="0" noresize/>
  <frame name="frame2" src="sample-2.html" scrolling="yes" frameborder="1" noresize/>
</frameset>
```

## Special Notes
**Frames are rarely used these days.** The introduction of server side scripting languages allow you to create content pages dynamically. The introduction of HTML5 has also provided new methods of doing page layouts without having to use frames. In fact, this tag has been removed from the Web standards. Though some browsers may still support it, it is in the process of being dropped. **Do not use it in old or new projects. Pages or Web apps; using it may break at any time.**

Even when the use of frames was defined in Web Standards, using it was not encouraged because of certain disadvantages such as performance problems and lack of accessibility for users with screen readers.