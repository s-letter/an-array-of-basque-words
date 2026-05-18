# an-array-of-basque-words

[English](./README.md) · [Euskera](./README.eu.md)

[![NPM version](https://img.shields.io/npm/v/an-array-of-basque-words.svg)](https://www.npmjs.com/package/an-array-of-basque-words)

List of ~4,655,000 Basque (Euskera) words.

Derived from the [Xuxen Basque Hunspell dictionary](http://xuxen.eus/)
(`eu_ES`), processed and filtered to include only clean alphabetic words using the Basque character set
(`[a-zñ]`).

Inspired by the architecture of [`an-array-of-english-words`](https://github.com/words/an-array-of-english-words)
by [Titus Wormer](https://github.com/wooorm).

## Install

```sh
npm install an-array-of-basque-words
```

## Use

```js
const words = require('an-array-of-basque-words')

console.log(words.length)     // ~N words
console.log(words.slice(0, 5))
// [ 'a', 'ab', ... ]

console.log(words.filter(w => w.startsWith('eusk')))
// [ 'euskal', 'euskaldun', 'euskara', ... ]
```

## API

The default export is a `string[]` of Basque words.

### TypeScript

Types are included:

```ts
import words = require('an-array-of-basque-words')

const filtered: string[] = words.filter(w => w.length === 5)
```

## Dataset

- **Source**: [Xuxen Basque Hunspell dictionary](http://xuxen.eus/static/hunspell/)
- **License**: GPL-2.0-or-later
- **Filter**: Only characters matching `/^[a-zñ]+$/`

## Build

To regenerate `index.json` from source:

```sh
node setup.js    # Download eu_ES.dic and eu_ES.aff from xuxen.eus
node expand.js   # Expand dictionary (memory-efficient, no external tools needed)
node build.js    # Clean, filter and generate index.json
```

## Credits

- **Linguistic data**: [Xuxen — Euskararen hiztegi arauemailea](http://xuxen.eus/)
- **Architectural pattern**: [Titus Wormer (@wooorm)](https://github.com/wooorm) — [`an-array-of-english-words`](https://github.com/words/an-array-of-english-words)

## License

GPL-2.0-or-later © Pablo G. Guízar
