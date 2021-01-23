<div align="center">
  <img width="180" height="180" vspace="20"
    src="https://cdn.worldvectorlogo.com/logos/css-3.svg">
  <a href="https://github.com/webpack/webpack">
    <img width="200" height="200"
      src="https://webpack.js.org/assets/icon-square-big.svg">
  </a>
</div>

# css-loader-with-hooks

The `css-loader-with-hooks` is a `css-loader` fork with access to internal loader data from webpack config

## Using hooks

**webpack.config.js**

```js
module.exports = {
  module: {
    rules: [
      {
        test: /\.css$/i,
        use: [
          "style-loader",
          {
            loader: "css-loader-with-hooks",
            options: {
              onExports : (exports, loaderContext) => {

              }
            }
        ],
      },
    ],
  },
};
```
