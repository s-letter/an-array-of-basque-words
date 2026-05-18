# an-array-of-basque-words

[English](./README.md) · [Euskera](./README.eu.md)

[![NPM version](https://img.shields.io/npm/v/an-array-of-basque-words.svg)](https://www.npmjs.com/package/an-array-of-basque-words)

~4.655.000 hitz euskarazkoen zerrenda.

[Xuxen euskara-hiztegi](http://xuxen.eus/) Hunspell-etik (`eu_ES`) eratorria, Euskarako karaktere-multzoa erabiliz hitz alfabetiko garbiak bakarrik sartzeko prozesatu eta iragazita (`[a-zñ]`).

[`an-array-of-english-words`](https://github.com/words/an-array-of-english-words) proiektuaren arkitekturan oinarrituta, [Titus Wormer](https://github.com/wooorm) garatzaileak egina.

## Instalazioa

```sh
npm install an-array-of-basque-words
```

## Erabilera

```js
const words = require('an-array-of-basque-words')

console.log(words.length)     // ~4655000
console.log(words.slice(0, 5))
// [ 'a', 'aachen', 'aachena', ... ]

console.log(words.filter(w => w.startsWith('euskar')))
// [ 'euskar', 'euskara', 'euskaradun', ... ]
```

## API

Exportazio nagusia Euskarako hitzen `string[]` bat da.

### TypeScript

Tipoak barne daude:

```ts
import words = require('an-array-of-basque-words')

const filtered: string[] = words.filter(w => w.length === 5)
```

## Datu-multzoa

- **Iturria**: [Xuxen — Euskararen hiztegi arauemailea](http://xuxen.eus/static/hunspell/)
- **Lizentzia**: GPL-2.0-or-later
- **Iragazkia**: `/^[a-zñ]+$/` betetzen duten karaktereak soilik

## Eraikuntza

`index.json` iturritik berriz sortzeko:

```sh
node setup.js    # eu_ES.dic eta eu_ES.aff deskargatu xuxen.eus-etik
node expand.js   # hiztegia hedatu (memoria-eraginkorra, kanpoko tresnarik gabe)
node build.js    # garbitu, iragazte eta index.json sortu
```

## Kredituak

- **Datu linguistikoak**: [Xuxen — Euskararen hiztegi arauemailea](http://xuxen.eus/)
- **Arkitektura-eredua**: [Titus Wormer (@wooorm)](https://github.com/wooorm) — [`an-array-of-english-words`](https://github.com/words/an-array-of-english-words)

## Lizentzia

GPL-2.0-or-later © Pablo G. Guízar
