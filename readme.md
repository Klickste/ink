![ink logo](./ink.svg)

Color tooling and core colors library.

[![npm publish](https://github.com/klickste/ink/actions/workflows/npm-publish.yml/badge.svg)](https://github.com/klickste/ink/actions/workflows/npm-publish.yml)
![npm (scoped)](https://img.shields.io/npm/v/@klickste/ink)

## Usage

Run `npm i @klickste/ink` in your project directory.

Use and (optionally) configure the Sass module:

```scss
@use '@klickste/ink' with (
  $namespace: 'acme',
  $useDarkMode: false,
  $useDisplayP3: false
);
```

Use the predefined modules:

```scss
@use '@klickste/ink/core';
@use '@klickste/ink/gray';

:root {
  @include core.palette;
  @include gray.palette;
}
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

:root {
  @include ink.colors($myPalette);
}
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
