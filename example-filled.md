# slug-it

Convert any string to a URL-safe slug. Handles unicode, emoji, and edge cases reasonably.

## The problem

Every project I write needs slug generation, and every npm slug package either pulls in 200KB of unicode tables or trips on a corner case I care about. Wrote a small one I trust.

## Quick example

```
import { slug } from 'slug-it';

slug("Hello, World!");           // "hello-world"
slug("Dr. Strangelove (1964)");  // "dr-strangelove-1964"
slug("Cafe au lait");            // "cafe-au-lait"
```

## Install

```
npm install slug-it
```

## Use it

```
import { slug } from 'slug-it';

const result = slug("Why I left Google", { maxLength: 30 });
// "why-i-left-google"
```

### `slug(input, options)`

- `input` (string, required), the string to convert
- `options.maxLength` (number, optional, default `60`), truncate at the nearest word boundary
- `options.separator` (string, optional, default `"-"`), the separator character
- Returns: a string, lowercased, with non-alphanumeric runs replaced by the separator

## What it doesn't do

- Does NOT preserve unicode characters as-is (everything is transliterated to ASCII)
- Does NOT guarantee uniqueness (combine with a counter or hash if needed)
- Does NOT support languages with non-Latin scripts well (CJK, Arabic, Hebrew). Use a localized package for those.

## Contributing

Issues and PRs welcome. Run `npm test` before submitting.

## Tech

Node 18+, zero runtime dependencies, ~80 lines of source.

## License

MIT. See [LICENSE](LICENSE).

## Related

- [github.com/sindresorhus/slugify](https://github.com/sindresorhus/slugify), fuller-featured alternative if you need more language support
