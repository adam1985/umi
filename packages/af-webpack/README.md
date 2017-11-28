# af-webpack

Unique webpack wrapper for ant financial (af).

## Why af-webpack ?

TODO

## CLIs based on af-webpack

* umi
* [roadhog@2](https://github.com/sorrycc/roadhog/tree/2.0)

## Configuration

See [./Configuration.md](./Configuration.md).

## API

### af-webpack/getConfig

Get webpack config with opts.

```js
const webpackConfig = getConfig(opts);
// use webpackConfig to dev or build
```

### af-webpack/dev

Run webpack-dev-server more gracefully with [react-dev-utils](https://github.com/facebookincubator/create-react-app/tree/master/packages/react-dev-utils).

```js
dev({
  webpackConfig,
  appName,
  extraMiddlewares,
  beforeServer,
});
```

webpackConfig is required, other optional.

Options:

* `webpackConfig`: the webpack config 
* `appName`: the default is "Your Project", text to show after dev server is started
* `extraMiddlewares`: extra middlewares for webpack-dev-server, based on express
* `beforeServer`: the function to execute before dev server is started

### af-webpack/build

Run webpack compilation.

```js
build({
  webpackConfig,
  success,
});
```

webpackConfig is required, other optional.

Options:

* `webpackConfig`: the webpack config 
* `success`: the function to execute after build is done successfully

### af-webpack/react-dev-utils

The APIs related to react-dev-utils.

* webpackHotDevClientPath：the real path of webpackHotDevClient

### af-webpack/webpack

The webpack, useful to register extra webpack plugins.

### af-webpack/registerBabel

Register babel for extra files.

## LICENSE

MIT