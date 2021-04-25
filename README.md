# Bedrocss

A foundational CSS library that's modern, lightweight, and easy to live with. It's somewhere between a [reset](https://cssdeck.com/blog/what-is-a-css-reset/) and a framework because resets don't do quite enough, and frameworks do a bit too much. Bedrocss applies sane defaults to plain HTML elements, so there isn't anything to learn, and it's super easy to modify.

- 1.6kb (795b zipped): Gets you going on the right foundation without any overhead.
- Minimal specificity: Super easy for you to customize without having to fight. 
- Incrementally Adoptable: If you don't like certain parts, you can leave them out.
- Slightly opinionated: For a solid foundation on which to grow your custom styles.

<a href="https://style-check.stegosource.com/?url=https://unpkg.com/bedrocss/bedrocss.min.css" style="display: inline-block; margin-top:1rem; border: 1px solid; border-radius: .25rem; padding: .25rem .5rem;">Demo</a>

<a href="https://github.com/austingil/bedrocss" style="display: inline-block; margin-top:1rem; border: 1px solid; border-radius: .25rem; padding: .25rem .5rem;">GitHub</a>

<a href="https://www.npmjs.com/package/bedrocss" style="display: inline-block; margin-top:1rem; border: 1px solid; border-radius: .25rem; padding: .25rem .5rem;">NPM</a>

## Installation

```
npm install bedrocss
```

<br>

```js
import 'bedrocss'
```

## Features

### Common Defaults

Every element will have `box-sizing: border-box;` by default, inherit the `system-ui` font, and have no margin or padding. Some tags (input, video, progres, and more) stretch the full width of their parents, and images are kept withing their parent elements.

### Easy to Customize

The library is made up of a few parts (see below) that you can easily opt out of. It defines CSS rules with tag and attribute selectors to maintain the lowest CSS specificity. This makes it easy be overwrite without having to write more specific rules, use `!important`, or anything complex.

### Typography

Headings have a fluid font size that adjusts to screen sizes. Helper classes (`h1, h2, h3, h4, h5, h6`) let you use the right semantic tag while styling like a different heading. Every element has a more comforable `line-height`.

### Accessibility Features

Uses rem units for any sizing to respect user's font-size preferences. Targets `prefers-reduces-motion` media query to disable animations, transitions, and animated scrolling for users that have declared they do not want it. This is especially relevant for users with vestibular disorders. Supports a basic dark mode out of the box based on user's system settings.

## Opting out of features

By default, when you import the library, you get everything. However, it's made up of a collection of files which you can pick out as you like. For example, to explicitly import all components, you could do:

```js
import 'bedrocss/src/base.css';
import 'bedrocss/src/typography.css';
import 'bedrocss/src/interactive.css';
import 'bedrocss/src/media.css';
```

<p style="margin-top: 30px; text-align: center;">
  Made with ❤ by
  <a href="https://austingil.com">Austin Gil</a>
</p>
