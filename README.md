# bedrocss

A classless CSS library that's modern, lightweight, and easy to modify so you can start your projects on a solid foundation. It does a bit more than a [reset](https://cssdeck.com/blog/what-is-a-css-reset/), but not so much as a framework. bedrocss applies sane defaults to plain HTML elements, so there isn't anything to learn, and it's super easy to modify.

- 933 bytes zipped (1.99kb unzipped): Gets you going on the right foundation without any overhead.
- Minimal specificity: Super easy for you to customize without having to fight. 
- Incrementally Adoptable: If you don't like certain parts, you can leave them out.
- Slightly opinionated: For a solid foundation on which to grow your custom styles.

<a href="https://style-check.austingil.com/?url=https://unpkg.com/bedrocss/bedrocss.min.css" style="display: inline-block; border: 1px solid; border-radius: .25rem; padding: .25rem .5rem;">Demo</a>
<a href="https://github.com/austingil/bedrocss" style="display: inline-block; border: 1px solid; border-radius: .25rem; padding: .25rem .5rem;">GitHub</a>
<a href="https://www.npmjs.com/package/bedrocss" style="display: inline-block; border: 1px solid; border-radius: .25rem; padding: .25rem .5rem;">NPM</a>

## Installation

The recommended approach is to include `bedrocss` as an NPM dependency.
```
npm install bedrocss
```

Then to include it in your application before any other CSS. 

```js
import 'bedrocss'
// other styles after
```

Alternatively, you can link to the unpkg CDN version from your HTML `<head>`. 

```html
<link rel="stylesheet" type="text/css" href="https://unpkg.com/bedrocss">
<!-- other styles after -->
```
## Features

### Common Defaults

Every project I've ever worked on sets `box-sizing: border-box;` on every element and the height of the app to match the screen height. Most others remove margin and padding on everything so there is a predictable starting point. Images have a max width of 100% so they don't break out of parent containers.

### User Focus

We style based on user preferences this by setting text to the  `system-ui` font, support light and dark mode with `color-scheme`, and if enabled, use the `prefers-reduces-motion` media query to disable animations and transitions. This is especially relevant for users with vestibular disorders.

### Accessibility

In addition to the reduced motion support above, this library has other accessibility features. It uses rem units for any sizing to respect user's font-size preferences. Better focus styles that handle border radius, use the user agent color, and still work in high-contrast mode.

### Slightly Opinionated

This library implements the most common practices as well as some opinions to make things easier. For example, many tags (input, video, progres, and more) stretch the full width of their parents. Although the margins are removed by default, we add some back for content flow so, for example, two paragraphs get some space between.

### Typography

Headings have a fluid font size that adjusts to screen sizes. Here are the only helper classes (`.h1, .h2, .h3, .h4, .h5, .h6`) so you can use the correct semantic HTML tag but style it like a different heading. Every element also has a `line-height` that's optimized for readability.

### Forms

Most inputs are set to take up the full width of their container. They also are set to inherit font styles rather than the default behavior of ignoring the body styles. Spacing, border, and colors are set to match as opposed to the default browser behavior with slightly different sizes. Visual feedback is provided for `disabled` and `readonly` inputs.

### Easy to Customize

Every CSS rule applies the lowest possible CSS specificity. This makes it easy be overwrite without having to write more specific rules, use `!important`, or anything complex. It's also is made up of a few parts (see below) that you can easily opt out of. 

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
