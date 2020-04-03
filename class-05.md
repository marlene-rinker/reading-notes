## Code 201 Reading Assignment Notes - Class 5

_April 3, 2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Images
_Chapter 5: “Images” (pp.94-125)_

[Choose the right images for your site](http://htmlandcssbook.com/extras/choosing-images-for-your-site/)

Best practice to store images in their own folder.

Three rules for creating images:

1. Save images in the right format (typically jpg, gif, or png)
2. Save images at the right size (same width and height it will appear on the website, measured in pixels)
3. Measure images in pixels

`<img>` is used to add an image on the page; it needs a `<src>` attribute to indicate the source of the image and an `<alt>' attribute to describe the image

Photographs are best saved as JPEGS; illustrations or logos that use flat colors are better saved as GIFs.

### Color
_Chapter 11: “Color” (pp.246-263)_

It's important to ensure there is enough contrast between text and background color so people can read the content.

The color on a computer screen is crated by mixing amounts of red, green, and blue.

You can use a color picker tool to find the color you want.

**RGB values** - values for red, green, and blue; expressed as numbers between 0 and 255; `rgb(102, 205, 170)`

**Hex codes** - values for red, green, and blue are expressed in hexadecimal code; `#66cdaa`

**Color names** - colors are represented by predefined names; these are limited (147 color names); `MediumAquaMarine`; not commonly used except for black and white

**Hue** - essentially the colloquial idea of color

**Saturation** - refers to the amount of gray in a color; maximum saturation = no gray, minimum saturation = mostly gray

**Brightness** - (aka "value") - refers to how much black is in a color; maximum brightness = no black, minimum brightness = very dark

**CSS3 introduces HSL colors (Hue Saturation Lightness)**

Hue and Saturation are the same as mentioned earlier. Lightness is not the same as Brightness.

**Lightness** - (sometimes called _luminosity_) is the amount of white (lightness) or black (darkness) in a color. It's expressed as a percentage. 0% lightness is black; 100% lightness is white; 50% lightness is normal. 

Brightness only adds black; Lightness offers both white and black.

### Text
_Chapter 12: “Text” (pp.264-299)_

#### Typeface terminology

**Serif** - extra details on the ends of the main strokes of the letters (serifs); typically used for long passages in print; (Georgia, Times, Times New Roman)

**Sans-serif** - straight ends on the letter, cleaner design; clearer to read if text is small (Arial, Verdana, Helvetica)

**Monospace** - every letter is the same width; commonly used for code because they align nicely and make the text easier to follow (Courier, Courier New)

**Cursive** - joining strokes or other cursive characteristics; (Comic Sans MS, Monotype Corsiva)

**Fantasy** - usually decorative fonts; often used for titles, not designed for long bodies of text (Impact, Haettenschweiler)

**Weight** - light, medium, bold, black; adds emphasis

**Style** - normal, italic, oblique; italic fonts have a cursive aspect to some of the lettering, oblique font styles take the normal style and put it on an angle

**Stretch** - condensed, regular, extended; condensed letters are thinner and closer together, extended letters are thicker and further apart

**Ascender** - above the cap height

**Cap Height** - top of flat letters

**X-Height** - height of the letter x

**Baseline** - line the letters sit on

**Descender** - below the baseline

#### Browser considerations

A browser will usually only display a typeface if it's installed on the computer. 

You can specify more than one typeface in order of preference. This is called a font stack. Example: `font-family: Georgia, Times, serif;` 

#### Text size

Use sizes from the longstanding type scale used by programs such as Word, Photoshop, and InDesign. 

The default size of text in a browser is 16 pixels.

Print designers refer to text size in points. A pixel roughly equates to a point in size.

You can set the size using pixels, percentages, and ems.

Pixels - best way to ensure the type appears at the size you intended

Percentages - allow you to create a scale; the text may appear in a larger size than intended if the user changes the default size of their text; the scale will be right though

Ems - allow you to change the size relative to the size of the text in the parent element; you can use similar rules as you would for percentages; the fonts could appear larger or smaller than intended if the user changes their default text size

Find conversions for 12 px scale and 16 px scale for each of these sizing options on p. 276.

Pseudo-classes - used to change the style an element when a user hovers over or clicks on text, or if they've visited a link (:link, :visited, :hover, :active, :focus)


---
[Home page](https://marlene-rinker.github.io/reading-notes/)