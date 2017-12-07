# Documentation Temple

## Author: Pramod

# Important Links
- [Woocommerce REST API Documentation link - Reference Website](http://woocommerce.github.io/woocommerce-rest-api-docs/#requirements)


# Libraries
- `http-server`: Simple Static Server to host files
- `node-sass`: SASS to CSS converter
- `node-sass-chokidar`: Not required, all SCSS transformation is handled by `node-sass` now
- `nodemon`: Node Monitor for live-compiling/compiling whenever source SCSS changes
- `npm-run-all`: Node plugin to run multiple scripts in parallel

> `package.json`

```js
{
  "name": "sass-documentation-layout",
  "version": "1.0.0",
  "description": "Simple sass project for a documentation layout",
  "main": "index.js",
  "scripts": {
    "build-css": "node-sass --include-path ./sass sass/main.scss public/css/styles.css",
    "watch-css": "nodemon -e scss -x \"npm run build-css\"",
    "static-server": "http-server",
    "start": "npm-run-all -p static-server watch-css"
  },
  "keywords": [],
  "author": "Pramod",
  "license": "MIT",
  "devDependencies": {
    "http-server": "^0.10.0",
    "node-sass": "^4.7.2",
    "node-sass-chokidar": "0.0.3",
    "nodemon": "^1.12.5",
    "npm-run-all": "^4.1.2"
  }
}
```

# Template
- Proper Layout Separation 
    - `Link Section` : Contains Links / Topics Navigation
    - `Content Section` : Contains documentation, points, important texts
    - `Code Section` : Contains Code Snippets

