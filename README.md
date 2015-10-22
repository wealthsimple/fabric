# Palette

Palette is the CSS toolkit that powers Wealthsimple's front-end design. It's purposefully limited to common components to provide our developers with the most flexibility. It's built with SCSS and available via Bower, so it's easy to include all or part of it within your own project.

[**Read the Palette documentation**](https://wealthsimple.github.io/palette/) to learn more.

## Install

Use [bower](http://bower.io/) to install the latest version of Palette on a project:

```
$ bower install --save git@github.com:wealthsimple/palette.git
```

### Usage

Once installed, simply `@import` either the master SCSS file, or the individual files as you need them.

```scss
// Example: All of Palette
@import "wealthsimple-palette/scss/palette";

// Example: Individual files
@import "wealthsimple-palette/scss/variables";
@import "wealthsimple-palette/scss/mixins";
@import "wealthsimple-palette/scss/base";
```
