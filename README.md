# Bedrocss

Bedrocss is a foundational CSS library that's modern, lightweight, and easy to customize. It's somewhere between a reset, a normalizer, and a framework. It's purpose is to make plain HTML elements look good by default, even the ones you didn't account for.

- 1.6kb (795b zipped)
- Minimal specificity
- Incrementally Adoptable
- Slightly opinionated

<a href="https://style-check.stegosource.com/?url=https://unpkg.com/bedrocss/bedrocss.min.css" style="border: 1px solid; border-radius: .25rem; padding: .25rem .5rem;">Demo</a>

## Installation

```
npm install bedrocss
```

```js
import 'bedrocss'
```

## Features

### Common Defaults

Every element will have `box-sizing: border-box;` by default, inheriting the `system-ui` font, and have no margin or padding. Images get a max width of 100%.

### Easy to Customize

The library is made up of a few components (see below) that you can easily opt out of. It defines CSS rules with tag and attribute selectors to maintain the lowest CSS specificity. This makes it easy be overwrite without having to write more specific rules, use `!important`, or anything complex.

### Typography

Headings have a fluid font size that adjusts to screen sizes. Helper classes (`h1, h2, h3, h4, h5, h6`) let you use the right semantic tag while styling like a different heading. Every element has a more comforable `line-height`.

### Slightly Opinionated

- Inputs, tables, videos, iframe and a few more default to 100% width.
- Without the padding, list bullets dont make sense.
- Interactive elements should look consistent.

### Accessibility Features

Uses `!important` with the `prefers-reduces-motion` media query to disable animations, transitions, and animated scrolling for users that have declared they do not want it. This is especially relevant for users with vestibular disorders. You can read more about this in <a href="https://css-tricks.com/introduction-reduced-motion-media-query/">this article</a> by <a href="https://twitter.com/ericwbailey">Eric Bailey</a>.

## Opting out of features

By default, when you import the library, you get everything. However, it's made up of a collection of files which you can pick out as you like. For example, to explicitly import all components, you could do:

```js
import 'bedrocss/src/base.css';
import 'bedrocss/src/typography.css';
import 'bedrocss/src/interactive.css';
import 'bedrocss/src/media.css';
```

<p style="margin-top: 30px; text-align: center;">
  <span style="clip: rect(0 0 0 0); clip-path: inset(50%); height: 1px; overflow: hidden; position: absolute; white-space: nowrap; width: 1px;">made</span>
  <span aria-hidden="true">&lt;/&gt;</span>
  with ❤ by
  <a href="https://austingil.com">Austin Gil</a>
</p>
