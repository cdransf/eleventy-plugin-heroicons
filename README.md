# `eleventy-plugin-heroicons`

[![npm](https://img.shields.io/npm/v/eleventy-plugin-heroicons.svg)](https://npmjs.com/package/eleventy-plugin-heroicons) [![npm bundle size (minified)](https://img.shields.io/bundlephobia/min/eleventy-plugin-heroicons.svg)](https://npmjs.com/package/eleventy-plugin-heroicons) [![npm](https://img.shields.io/npm/dt/eleventy-plugin-heroicons.svg)](https://npmjs.com/package/eleventy-plugin-heroicons)

🛡 Shortcodes to add [Heroicons](https://heroicons.com/) to your [Eleventy](https://11ty.dev) projects

## Get started

Install the package:

```sh
npm i -D eleventy-plugin-heroicons
```

Then add the plugin to your `.eleventy.js` file:

```js
// .eleventy.js
module.exports = eleventyConfig => {
    eleventyConfig.addPlugin(require('eleventy-plugin-heroicons'));
}
```

## Usage

This plugin adds three shortcodes: `heroicon`, `heroicon-outline`, and `heroicon-solid`.

### `heroicon`

Args: `style: ("outline"|"solid")`, `name: string`, `alt?: string`

```md
{% heroicon "outline" "archive" %}
{% heroicon "solid" "x" "Close menu" %}
```

### `heroicon-outline`/`heroicon-solid`

These wrap the `heroicon` shortcode and pass a style.

Args: `name: string`, `alt?: string`

```md
{% heroicon-outline "x" "Close menu" %}
{% heroicon-solid "archive" %}
```

## Configuration

`eleventy-plugin-heroicons` offers a few options on a configuration object passed to Eleventy's `addPlugin()`:

- `className?: string` Adds a class to all heroicons
- `errorOnMissing: boolean` (default: `false`) Throw an error when passed an invalid style/name

Pass the configuration object when adding the plugin:

```js
// .eleventy.js
module.exports = eleventyConfig => {
    eleventyConfig.addPlugin(require('eleventy-plugin-heroicons'), {
        className: 'icon',
        errorOnMissing: true
    });
}
```

## License

[MIT](./LICENSE) © [Sean McPherson](https://seanmcp.com)
