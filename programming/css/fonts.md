== Typeface ==
Typeface: distinctive design that's common to any related set of letters, numbers and symbols.
A font is a particular implementation of a typeface, meaning tyep typeface as rendered with a specific size, weight, and style.

Helvetica is a typeface. Helvetica 16-point bold is a font.

5 main categorie to distinguish most typefaces:
- Serif: contains fine cross strokes (called feet) at the extremities of each character. Give traditional, classy look. Get lost when displayed on a screen at small sizes.
- Sans serif: Doesn't contain cross strokes on the extremities of characters. usually have a clean, modern look that's well suited to screen text, particularly at small sizes.
- Monospace: fixed-width - uses the same amount of space for each character. Skinny characters (i, l), take same space as wider letters (m, w)
- Cursive: resembles handwritten pen or brush writing
- Fantasy - fanciful designs - extreme elements (like extra thick)

Serif: works best for headings, other text set at large sizes
Sans serif: works best for body text
Monospace: works well for code listings
Cursive: best for short bits of text that require elegance or playfulness
Fantasy: for special effect

Css property for typeface: font-family

# generic fonts: impelemted by all browsers: sans, sans serif, monospace, cursive, fantasy
font-family: sans-serif

# system font (installed by site visitor)
Using quotation marks and capitalizing the first letter of each word in a system font name are optional, but good habits.
If font name includes spaces, nubmers or punctuations other than hypen(-) use quotation marks:
font-family: "Times New Roman";
Capitalize the first letter:
font-family: Georgia;

You can specify more than one font names separated by comma. Browser ches the fonts in the specified order, uses the first one installed on the user's computer.

Good practive to include a similar generic font family after the system font.
font-family: "Times New Roman", Georgia, serif;

Most installed fonts:
sans-serif: Arial, Arial Black, Tahoma, Trebuchet MS, Verdana
serif: Georgia, Times New Roman
monospace: Courier New

https://www.cssfontstack.com

== type size ==
font-size: <value>

value: pixels, em, rm

font-size: 24px

- bold
font-weight values:
100, 200, 300, 400(normal), 500, 600, 700(bold), 800, 900

- italics
font-style: italic


# font
font-size: 36px
text-align: center;
font-variant: small-caps



good sans-serif fonts: Optima, Calibri
