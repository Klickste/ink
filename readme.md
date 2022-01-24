![ink logo](./ink.svg)

Color tooling and core colors library.

[![npm publish](https://github.com/klickste/ink/actions/workflows/npm-publish.yml/badge.svg)](https://github.com/klickste/ink/actions/workflows/npm-publish.yml)

## Usage

Run `npm i @klickste/ink` in your project directory.

Use and (optionally) configure the Sass module:

```scss
@use '@klickste/ink' with (
  $namespace: 'acme',
  $selector: 'body',
  $useDarkMode: false,
  $useDisplayP3: false
);
```

Use the predefined core colors module:

```scss
@use '@klickste/ink/core';
```

### Use the built-in mixins

Declare your own color palette:

```scss
$myPalette: (
  'light': (
    'brand': rgb(242 59 34),
  ),
  'dark': (
    'brand': rgb(222 35 19),
  ),
);

@include ink.colorPalette($myPalette);
```

Declare a single color:

```scss
:root {
  // RGB color
  @include ink.color('brand', rgb(242 59 34));

  // Display P3 color
  @include ink.color('brand', rgb(242 59 34), true);
}
```
