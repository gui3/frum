# frum

**FR**om a n**UM** make great things.

> Inspired by ruby number methods

Extend a number to offer useful functions

```js
// create ranges
let range = frum(3).to(7.4)

// iter loops or create array
range.by(0.1, mappingOrCallback )

// test overlappings
// range.intersects( frum(1).to(4) ) // true - not implemented yet
range.contains(8) // false

// and many more to come...

// ...even a ruby '5.times do' equivalent
frum(5).count(callback) // ?target=0, ?step=1
// for lazy loops (and happy developper)
```

> **Date** and other types support is not working,
> but it's a mid-term goal.


# Install

> the same routine as always

There are **NO dependancies**,
the code used tries to be **non ES6**
so that it could **run on older browsers**. Let me know if I made mistakes.

> cross compatibility node/browser thanks to moment.js

- Usable in browser

```html
<script type="text/javascript" src="path/to/frum/index.js"></script>
```

*There is no CDN for now but it might come if you ask for it.*

- Usable in node

```
npm install frum
```

```js
const frum = require('frum')
```


# Use (not written yet)

> as simple as that

for now there is a **trailing decimal** problem
when you use decimals you might come across
`x.000000000006` numbers that are **not what you wanted**

This is a [known issue from javascript](https://stackoverflow.com/questions/1458633/how-to-deal-with-floating-point-number-precision-in-javascript)
and I will fix that later

**[test me in the browser console](https://gui3.github.io/frum/.)**

```js

const frum = require('frum'); //from node

//making ranges
let range = frum(3).to(7.4)

// iterating
range.by(2, console.log )

// creating arrays
range.by(2) //simple

range.by(2, function (i) {
  return 'I said ' + i + ' ! ' // mapping
})

// overlappings
range.contains(8) // false

// and lazy loops
frum(5).count(console.log) // ?target=0, ?step=1

// ------------------

// the most lazy case :
frum(5).count(callback)
// IS THE SAME AS :
for (let i = 0, i < 5, i++) {
  callback( i )
}


```
