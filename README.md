# Values.js

The lightness or darkness of a color is called its value.
Tints are light values that are made by mixing a color with white, which increases lightness.
Shades are dark values that are made by mixing a color with black, which reduces lightness.

## Dependencies
None

## Usage Example
```js
// include values.js to your project
<script src="values.js"></script>
```

```js
var color = new Values('#0099ff');
var values = color.getTintsAndShades();
for (var i = 0; i < values.length; i += 1) {
    console.log( values[i] );
}
```

## Methods

#### Get Tints ( include_base_color = false : boolean )
```js
var tints = color.getTints();
// returns an array of objects width the tints
/*
 * The base color is excluded by default.
 * You can include the base color to the results passing true as an argument.
 * ex: color.getTints( true )
*/
```

#### Get Shades ( include_base_color = false : boolean )
```js
var shades = color.getShades();
// returns an array of objects with the shades (Base color is excluded)
/*
 * The base color is excluded by default.
 * You can include the base color to the results passing true as an argument.
 * ex: color.getShades( true )
*/
```

#### Get Both tints and shades
```js
var allValues = color.getTintsAndShades();
// returns an array of objects with both the tints and shades (Base color always included)
```

#### Lightness ( value : number, include_base_color = false : bolean )
Accepts a positive or negative number
```js
var lighten = color.lightness( 20 );
// returns an array with a single object ith lightnedd increased
// => [{ hex: "#33ccff", hsl: { h: 195, s: 100, l: 60 }, rgb: { r: 51, b: 255, g: 204 }]

var darken = color.lightness( -20 );
// returns an array with a single object with lightness decreased
// => [{ hex: "#004d66", hsl: { h: 195, s: 100, l: 20 }, rgb: { r: 0, b: 102, g: 77 }]

/*
 * The base color is excluded by default.
 * You can include the base color passing true as an argument.
 * ex: color.lightness( 20, true )
 * will return an array with two objects, the original and the modified.
*/
```

#### Get Color
```js
var current = color.getColor();
```

#### Get range (percentage)
```js
var range = color.getRage();
```

#### Change Base Color
```js
color.setColor('#ff0000');
```

#### Change range (percentage)
```js
color.setRange( 10 );
```

## Defaults Options
```js
color: {
    hex: "#37D7C2",
    rgb: {r: 55,  g: 215, b: 194, text: 'rgb(55, 215, 194)' },
    hsl: {h: 172, s: 67,  l: 53,  text: 'hsl(172, 67%, 53%)'}
},
range: 1
```
