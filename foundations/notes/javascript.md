# JavaScript

## Integration

```<script></script>``` = type javascript code inside this element of an html file.

```<script src="javascript.js></script>``` = links to an external javascript file.

## Keywords

```let``` = variable keyword.

```js
let message;

message = 'Hello'; // store string "hello" in variable named message.

let user = 'John' // comma-first style
  , age = 25
  , message = 'Hello';
```

```var``` = old version of ```let```

```js
var message = 'Hello';
```

```const``` = creates constant variables.

```js
const PI = 3.141592653;
```

## Types

### Primatives

```Number``` = 64bit double precision data structure that can hold integers and floats.

```BigInt``` = Arbitrary length precise number.  denoted by adding an 'n' at the end of a number.

```String``` = An array of characters enclosed in double quotes: ```''im a string''```.

```Boolean``` = Binary data type that equates to ```true``` or  ```false```.

```null``` = Unary data type that represents nothing.

```undefined``` = Unary data type that represents a value not being assigned anything.

```symbol``` = Creates a unique identifier for objects

### Non-Primatives

```object``` = Holds a collection of data and complex entities

## Commands

```console.log()``` = print something to the developer console in browser

```js
console.log("Hello, World!");
```

```typeof``` or ```typeof()``` = returns the type of an operand.

### strings

All string methods return a new string, as strings are immutable.

#### Extracting string characters:

```at(position)``` = Returns the character at a specified index in a string. (Allows negatives)

```charAt(position)``` = Returns the character at a specified index in a string. (Disallows negatives)

```charCodeAt(position)``` = Returns the (ASCII)code of the character at a specified index in a string.

```[]``` = Read only access to an index position of a string.

#### Extracting string parts:

```slice(start, end)``` = extracts a part of a string and returns the extracted part in a new string.  If 'end' is ommitted, then rest of string is taken.  if param is negative, it is counted from end of string.

```substring(start, end)``` = same as slice, but start and end values less than 0 are treated as 0.

```substr(start, length)``` = same as slice, but second param specifies length of string, not endpoint.

#### Convert to upper and lower case:

```toUpperCase()``` = sets all characters to uppercase.

```toLowerCase()``` = sets all characters to lowercase.

#### String Concat:

```concat()``` = joins two or more strings.  Can be used in place of the binary ```+``` operator.

#### Trim Whitespace from String:

```trim()``` = removes whitespace from both sides of a string.

```trimStart()``` = removes whitespace from start of string.

```trimEnd``` = removes whitespace from end of string

#### Pad String:

```padStart(length, "pad")``` = adds ```pad``` to start of string over a given length.

```padEnd(lengthm "pad")``` = adds ```pad``` to end of string over a given length.

#### Repeat and Replace:

```repeat(count)``` = returns a string with a number of copies of a string.

```replace("To Replace", "Replacer")``` = replaces first specified value with another value in a string.

```
Regular Expressions (no quotes):

/i = case insensitive

/g = replace all matches
```

```replaceAll(To Replace, Replacer)``` = like using /g with ```replace()```

#### Convert to Array

```split(delimiter)``` = converts string to an array, splitting at the specified delimiter.

## Conditionals

Just like any other C based language.