This repository exercises functionality of Webpack 4 to create multiple output bundles that do not duplicate code.

The goal is to produce `dist/main.bundle.js` from the `src/index.js` entrypoint, but *not* include in the bundle the contents of `src/client_config.js`, which should be loaded separately.

In other words, the value of `SETTING` exported by `src/client_config.js` should *not* appea in the `dist/main.bundle.js`:

    grep -q ABRACADABRA dist/main.bundle.js && echo "failed"

See also the [Code Splitting guide](https://v4.webpack.js.org/guides/code-splitting/).
