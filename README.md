# frum

> FRom a nUM make great things.
> Inspired by ruby number methods

Extend a number to offer useful functions

```js
// create ranges
let range = frum(3).to(7.4)

// iter loops or create array
range.by(0.1, mappingOrCallback )

// test overlappings
range.intersects( frum(1).to(4) ) // true
range.contains(8) // false

// and many more to come...

// ...even a ruby '5.times do' equivalent
frum(5).count(callback) // ?target=0, ?step=1
// for lazy loops (and happy developper)
```

> **Date** and other types support is not working,
> but it's a mid-term goal.

# Use

> as simple as that

[test it in the browser console](#index.js)

```js

const frum = require('frum'); //from node

// for the exemples sake
// here is a callback function :
function callback ( val, index ) {
  console.log( 'v: ' + val + '| i: ' + index )
}

// actual examples ----------

frum(3).to(8).do( callback )

// IS THE SAME AS :
let ix = 0;
for (let i = 3, i <= 8, i += 1) {
  callback(i, ix);
  ix += 1;
}

// the most lazy case :
frum(5).reach( callback )
// IS THE SAME AS :
for (let i = 0, i < 5, i++) {
  callback( i, i ) // 2 times because index
}

frum(4)

frum(8)

```

# Installation

> the same routine as always

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
