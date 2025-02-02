# CSS Cheat Sheet

## CSS2 Selectors

| Selector | Description |
|----------|-------------|
| **`*`** | All elements |
| **`div`** | `<div>` element |
| **`div *`** | All elements within `<div>` |
| **`div span`** | `<span>` within `<div>` |
| **`div, span`** | `<div>` and `<span>` |
| **`div > span`** | `<span>` with parent `<div>` |
| **`div + span`** | `<span>` preceded by `<div>` |
| **`.class`** | Elements of class "class" |
| **`div.class`** | `<div>` of class "class" |
| **`#itemid`** | Element with id "itemid" |
| **`div#itemid`** | `<div>` with id "itemid" |
| **`a[attr]`** | `<a>` with attribute "attr" |
| **`a[attr='x']`** | `<a>` when "attr" is "x" |
| **`a[class~='x']`** | `<a>` when class is a list containing 'x' |
| **`a[lang|='en']`** | `<a>` when lang begins "en" |

## CSS2 Pseudo Selectors and Pseudo Classes

| Selector | Description |
|----------|-------------|
| **`:first-child`** | First child element |
| **`:first-line`** | First line of element |
| **`:first-letter`** | First letter of element |
| **`:hover`** | Element with mouse over |
| **`:active`** | Active element |
| **`:focus`** | Element with focus |
| **`:link`** | Unvisited links |
| **`:visited`** | Visited links |
| **`:lang(var)`** | Element with language "var" |
| **`:before`** | Before element |
| **`:after`** | After element |

## CSS2 Sizes

| Size | Description |
|------|-------------|
| **`0`** | No unit required |
| **`em`** | Equal to font size of parent (same as 100%) |
| **`ex`** | Height of lowercase "x" |
| **`%`** | Percentage |
| **`px`** | Pixels |
| **`cm`** | Centimeters |
| **`mm`** | Millimeters |
| **`in`** | Inches |
| **`pt`** | 1pt = 1/72in |
| **`pc`** | 1pc = 12pt |

## CSS2 Colors

| Color Format | Description |
|--------------|-------------|
| **`#789abc`** | RGB Hex Notation |
| **`#acf`** | Shortened hex notation |
| **`rgb(0, 25, 50)`** | RGB with values between 0-255 |
| **`rgb(0%, 10%, 20%)`** | RGB with percentages |

## CSS2 Box Model & Positioning

| Property | Description |
|----------|-------------|
| **`display`** | Defines the display style (block, inline, etc.) |
| **`clear`** | Specifies if elements should clear previous floats |
| **`position`** | Specifies positioning method (static, relative, absolute) |
| **`z-index`** | Specifies the stacking order of elements |
| **`top`** | Top offset for positioned elements |
| **`right`** | Right offset for positioned elements |
| **`bottom`** | Bottom offset for positioned elements |
| **`left`** | Left offset for positioned elements |
| **`overflow`** | Defines behavior of overflowed content |
| **`clip`** | Defines a clipping region for an element |
| **`float`** | Specifies floating elements |
| **`visibility`** | Specifies visibility of an element |

## CSS2 Dimensions

| Property | Description |
|----------|-------------|
| **`width`** | Specifies the width of an element |
| **`height`** | Specifies the height of an element |
| **`min-width`** | Minimum width of an element |
| **`max-width`** | Maximum width of an element |
| **`min-height`** | Minimum height of an element |
| **`max-height`** | Maximum height of an element |
| **`vertical-align`** | Aligns an element vertically |

## CSS2 Colors and Background

| Property | Description |
|----------|-------------|
| **`color`** | Sets text color |
| **`background-color`** | Sets background color |
| **`background-image`** | Sets a background image |
| **`background-repeat`** | Defines how the background image repeats |
| **`background-position`** | Defines the starting position of the background image |
| **`background-attachment`** | Defines how the background image scrolls with the page |

## CSS2 Text

| Property | Description |
|----------|-------------|
| **`text-indent`** | Indentation for the first line of text |
| **`text-align`** | Aligns text (left, right, center, justify) |
| **`text-transform`** | Controls text case (uppercase, lowercase) |
| **`text-decoration`** | Adds decoration to text (underline, line-through) |
| **`white-space`** | Controls how whitespace inside an element is handled |
| **`text-shadow`** | Adds a shadow to text |
| **`line-height`** | Specifies the height of lines in text |
| **`letter-spacing`** | Sets space between letters |

## CSS2 Fonts

| Property | Description |
|----------|-------------|
| **`font-family`** | Specifies the font to use |
| **`font-size`** | Specifies the font size |
| **`font-weight`** | Specifies the font weight (normal, bold) |
| **`font-style`** | Specifies the font style (normal, italic) |
| **`font-variant`** | Specifies a variant of the font (e.g., small-caps) |

## CSS2 Box Model Properties

| Property | Description |
|----------|-------------|
| **`margin`** | Sets margin around an element |
| **`padding`** | Sets padding inside an element |
| **`border`** | Sets the border around an element |
| **`border-width`** | Defines the width of the border |
| **`border-color`** | Defines the color of the border |
| **`border-style`** | Defines the style of the border (solid, dotted) |

## CSS2 Miscellaneous

| Property | Description |
|----------|-------------|
| **`list-style-type`** | Defines the type of list marker (e.g., disc, square) |
| **`cursor`** | Defines the type of cursor when hovering over an element |
| **`outline`** | Specifies the outline around an element |

