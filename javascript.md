# JavaScript Cheat Sheet

## Regular Expressions Syntax

| Expression | Description |
|------------|-------------|
| **`^`** | Start of string |
| **`$`** | End of string |
| **`.`** | Any single character |
| **`(a|b)`** | a or b |
| **`(...)`** | Group section |
| **`[abc]`** | In range (a, b or c) |
| **`[^abc]`** | Not in range |
| **`\s`** | White space |
| **`a?`** | Zero or one of a |
| **`a*`** | Zero or more of a |
| **`a*?`** | Zero or more, ungreedy |
| **`a+`** | One or more of a |
| **`a+?`** | One or more, ungreedy |
| **`a{3}`** | Exactly 3 of a |
| **`a{3,}`** | 3 or more of a |
| **`a{,6}`** | Up to 6 of a |
| **`a{3,6}`** | 3 to 6 of a |
| **`a{3,6}?`** | 3 to 6 of a, ungreedy |
| **`\\`** | Escape character |
| **`[:punct:]`** | Any punctuation symbol |
| **`[:space:]`** | Any space character |
| **`[:blank:]`** | Space or tab |

### Pattern Modifiers

| Modifier | Description |
|----------|-------------|
| **`g`** | Global match |
| **`i`** | Case-insensitive |
| **`m`** | Multiple lines |
| **`s`** | Treat string as a single line |
| **`x`** | Allow comments and whitespace in pattern |
| **`e`** | Evaluate replacement |
| **`U`** | Ungreedy pattern |

### JavaScript RegExp Object Methods

| Method | Description |
|--------|-------------|
| **`compile()`** | Recompiles the regular expression |
| **`exec()`** | Executes a match and returns results |
| **`test()`** | Tests if pattern exists in string |
| **`lastIndex`** | Returns the last index matched |
| **`lastMatch`** | Returns the last match found |
| **`lastParen`** | Returns the last captured group |

## JavaScript Event Handlers

| Event Handler | Description |
|---------------|-------------|
| **`onabort`** | Triggered when an operation is aborted |
| **`onmousedown`** | Mouse button pressed down |
| **`onblur`** | When an element loses focus |
| **`onmouseover`** | When mouse pointer hovers over an element |
| **`onclick`** | When an element is clicked |
| **`onkeydown`** | When a key is pressed down |
| **`onkeyup`** | When a key is released |
| **`onload`** | When the page or image is loaded |

## JavaScript Arrays

| Method | Description |
|--------|-------------|
| **`concat()`** | Combines two or more arrays |
| **`slice()`** | Returns a shallow copy of a portion of an array |
| **`join()`** | Joins elements of an array into a string |
| **`sort()`** | Sorts the elements of an array |
| **`push()`** | Adds an element to the end of an array |
| **`pop()`** | Removes the last element from an array |

## JavaScript Numbers and Maths

| Method | Description |
|--------|-------------|
| **`abs()`** | Returns the absolute value |
| **`max()`** | Returns the largest number |
| **`min()`** | Returns the smallest number |
| **`pow()`** | Returns base raised to the power of exponent |
| **`sqrt()`** | Returns the square root |
| **`random()`** | Returns a random number between 0 and 1 |

## JavaScript Booleans

| Method | Description |
|--------|-------------|
| **`toSource()`** | Returns a string representing the Boolean object |
| **`valueOf()`** | Returns the primitive value of a Boolean |

## JavaScript Dates

| Method | Description |
|--------|-------------|
| **`Date()`** | Returns the current date and time |
| **`getDate()`** | Gets the day of the month |
| **`getDay()`** | Gets the day of the week |
| **`setFullYear()`** | Sets the year for a date object |
| **`setTime()`** | Sets the date and time in milliseconds |

## JavaScript Strings

| Method | Description |
|--------|-------------|
| **`charAt()`** | Returns the character at a specified position |
| **`indexOf()`** | Returns the position of the first occurrence of a substring |
| **`toLowerCase()`** | Converts a string to lowercase |
| **`toUpperCase()`** | Converts a string to uppercase |
| **`replace()`** | Replaces occurrences of a substring with another |

## JavaScript Functions

| Method | Description |
|--------|-------------|
| **`decodeURI()`** | Decodes a URI string |
| **`isNaN()`** | Checks if a value is NaN |
| **`encodeURI()`** | Encodes a URI string |
| **`parseInt()`** | Converts a string to an integer |
| **`eval()`** | Executes a string of code |

