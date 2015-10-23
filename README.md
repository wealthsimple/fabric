# Fabric

Fabric is the CSS toolkit that powers Wealthsimple's front-end design. It's purposefully limited to common components to provide our developers with the most flexibility. It's built with SCSS and available via Bower, so it's easy to include all or part of it within your own project.

[**Read the Fabric documentation**](http://fabric.wealthsimple.com/) to learn more.

## Install

### Option 1. Bower

We recomend using [bower](http://bower.io/) for frontend package management. First, create a `bower.json` in your project root directory if you dont have one yet:

```json
{
  "name": "your-project-name",
  "private": true
}
```

Then, to install the latest version of Fabric, run:

```
$ bower install --save git@github.com:wealthsimple/fabric.git
```

To update the package once installed:

```
$ bower update wealthsimple-fabric
```

### Option 2. Minified CSS

The concatenated and minified CSS is available in https://github.com/wealthsimple/fabric/blob/master/css/fabric.css

Note: this is recommended against, as you won't have access to any of the SCSS variables or mixins.

## Usage

Once installed with bower, simply `@import` either the master SCSS file, or the individual files as you need them.

```scss
// Example: All of Fabric
@import "wealthsimple-fabric/scss/fabric";

// Example: Individual files
@import "wealthsimple-fabric/scss/variables";
@import "wealthsimple-fabric/scss/mixins";
@import "wealthsimple-fabric/scss/base";
```

## Fonts

Since font installation may vary based on the asset compilation framework you're using (e.g. Sprockets for Rails, Grunt for Ghost.org), Fabric does not include `@font-face` definitions. You must include these yourself.

Example below. Note: for Sprockets-based compilation, you'll want to replace `url` with `font-url`.

```scss
@font-face {
  font-family: 'FuturaBT-Light';
  src: url('/fonts/2F4FAE_0_0.eot');
  src: url('/fonts/2F4FAE_0_0.eot?#iefix') format('embedded-opentype'),url('/fonts/2F4FAE_0_0.woff2') format('woff2'),url('/fonts/2F4FAE_0_0.woff') format('woff'),url('/fonts/2F4FAE_0_0.ttf') format('truetype');
}

@font-face {
  font-family: 'FuturaBT-Book';
  src: url('/fonts/2F4FAE_1_0.eot');
  src: url('/fonts/2F4FAE_1_0.eot?#iefix') format('embedded-opentype'),url('/fonts/2F4FAE_1_0.woff2') format('woff2'),url('/fonts/2F4FAE_1_0.woff') format('woff'),url('/fonts/2F4FAE_1_0.ttf') format('truetype');
}

@font-face {
  font-family: 'FuturaBT-Heavy';
  src: url('/fonts/2F4FAE_2_0.eot');
  src: url('/fonts/2F4FAE_2_0.eot?#iefix') format('embedded-opentype'),url('/fonts/2F4FAE_2_0.woff2') format('woff2'),url('/fonts/2F4FAE_2_0.woff') format('woff'),url('/fonts/2F4FAE_2_0.ttf') format('truetype');
}

@font-face {
  font-family: 'CaslonGraD';
  src: url('/fonts/2F4FAE_3_0.eot');
  src: url('/fonts/2F4FAE_3_0.eot?#iefix') format('embedded-opentype'),url('/fonts/2F4FAE_3_0.woff2') format('woff2'),url('/fonts/2F4FAE_3_0.woff') format('woff'),url('/fonts/2F4FAE_3_0.ttf') format('truetype');
}
```

## Credits

Boilerplate for this repository was heavily reused from GitHub's own CSS toolkit: https://github.com/primer/primer
