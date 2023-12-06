# rn-image-auto-height

this is a fork of [vivaxy](https://github.com/vivaxy/react-native-auto-height-image).. I just upgraded the package dependencies. Orginal npm package name was also changed from react-native-auto-height-image to rn-image-auto-height.

Initialized by [vivaxy/gt-npm-package](https://github.com/vivaxy/gt-npm-package)

[![NPM Version](http://img.shields.io/npm/v/rn-image-auto-height.svg?style=flat-square)](https://www.npmjs.com/package/rn-image-auto-height)
[![NPM Downloads](https://img.shields.io/npm/dt/rn-image-auto-height.svg?style=flat-square)](https://www.npmjs.com/package/rn-image-auto-height)
[![MIT License](https://img.shields.io/npm/l/rn-image-auto-height.svg?style=flat-square)](./LICENSE)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg?style=flat-square)](https://conventionalcommits.org)
[![Financial Contributors on Open Collective](https://opencollective.com/rn-image-auto-height/all/badge.svg?label=financial+contributors&style=flat-square)](https://opencollective.com/rn-image-auto-height)
[![Maintainers Wanted](https://img.shields.io/badge/maintainers-wanted-red.svg?style=flat-square)](https://github.com/vivaxy/rn-image-auto-height/issues/88)
[![DOI](https://zenodo.org/badge/89235823.svg)](https://zenodo.org/badge/latestdoi/89235823)

This component provides you a simple way to load a remote image and automatically set `Image` height to the image dimension which fits the provided width.

React Native `Image` component needs users to set both `width` and `height` props.

React Native version requirements: >=0.72.6.

## Installation

`yarn add rn-image-auto-height`

`npm install rn-image-auto-height`

## Usage

Use local or remote files:

```js
import React, { Component } from 'react';
import AutoHeightImage from 'rn-image-auto-height';

import image from 'gallifrey-falls.png';

export default class Demo extends Component {
  render() {
    return (
      <View>

        <AutoHeightImage
          width={100}
          source={image}
        />

        <AutoHeightImage
          width={100}
          source={{uri: 'http://placehold.it/350x150'}}
        />

      </View>
    );
  }
}
```

You can even specify fallback images for when the source fails to load:

```js
import React, { Component } from 'react';
import AutoHeightImage from 'rn-image-auto-height';

import image from 'gallifrey-falls.png';

export default class Demo extends Component {
  render() {
    return (
      <AutoHeightImage
        width={100}
        source={{uri: 'https://vivaxy.github.io/404'}}
        fallbackSource={image}
      />
    );
  }
}
```

### Props

| name               | type             | isRequired    | default           | description                                                           |
| ---                | ---              | ---           | ---               | ---                                                                   |
| `width`            | number           | ✔             | N/A               | image width to fit                                                    |
| `maxHeight`            | number           | ✖             | `Infinity`               | image max height                                                    |
| `source`           | number or object | ✔             | N/A               | local (i.e. require/import) or remote image ({uri: '...'})            |
| `fallbackSource`   | number or object | ✖             | N/A               | local (i.e. require/import) or remote image ({uri: '...'})            |
| `onHeightChange`   | func             | ✖             | `(height) => {}`    | called when updating image height, the argument `height` might be `0` |
| `animated`        | bool              | ✖              | `false`               | Use `Animated.Image` instead of `Image` |

Other [image props](https://reactnative.dev/docs/image#props) except `resizeMode` are accepted.

## Change Log

[Change log](./CHANGELOG.md)

## Contributing

[Contributing](./CONTRIBUTING.md)

## Licence

[MIT](./LICENSE)

## Contributors

### Code Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
<a href="https://github.com/vivaxy/rn-image-auto-height/graphs/contributors"><img src="https://opencollective.com/rn-image-auto-height/contributors.svg?width=890&button=false" /></a>

### Financial Contributors

Become a financial contributor and help us sustain our community. [[Contribute](https://opencollective.com/rn-image-auto-height/contribute)]

#### Individuals

<a href="https://opencollective.com/rn-image-auto-height"><img src="https://opencollective.com/rn-image-auto-height/individuals.svg?width=890"></a>

#### Organizations

Support this project with your organization. Your logo will show up here with a link to your website. [[Contribute](https://opencollective.com/rn-image-auto-height/contribute)]

<a href="https://opencollective.com/rn-image-auto-height"><img src="https://opencollective.com/rn-image-auto-height/organization.svg?width=890"></a>

## Related Projects

- [react-native-scalable-image](https://github.com/ihor/react-native-scalable-image)
- [react-native-fit-image](https://github.com/huiseoul/react-native-fit-image)
- [react-native-responsive-image-view](https://github.com/wKovacs64/react-native-responsive-image-view)
- [react-native-auto-image](https://github.com/egorshulga/react-native-auto-image)
