= images =

# Aligning images and text
<img> tag is inline element. By default, the bottom edge of the image aligns with the baseline of the current line. You can control it via vertical-align property:

vertical-align: baseline | bottom | middle | top;
You can specify a length value (in pixels) for finer control. To move the image up, specify a negative value.


# backgroung images
background-image: url(/images/bg.png);

background-repeat: repeat | repeat-x | repeat-y | not-repeat
By default, browser repeats a image horizontally and vertically until the element is filled (tiling).

background-position: x y;
By default, tiling starts in the top-left corner of the parent element.
x: horizontal position pixel or percentage or left, center, right
vertical: vertical positon in pixel or percentage or top, center, bottom
backgorund-position: left top; (default)

# Hero image
an eye-catching photo or illustration that takes up the entire width and usually enire height of the browser window when you first land of a page.
Steps for hero image:
1. begin with div: width: 100vw, height: 100vh
    vw : one one-hundredth of the browser window's width
    vh: one one-hundredth of the browser window's height
2. div : background-position: center center;
3. div: background-size: cover (sizes the image so that it covers the entire background of the block element)

# Background shorthand property
background: background-color background-image background-repeat background-attachment background-position

