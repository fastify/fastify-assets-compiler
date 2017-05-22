# fastify-assets-compiler

[![Greenkeeper badge](https://badges.greenkeeper.io/fastify/fastify-assets-compiler.svg)](https://greenkeeper.io/)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](http://standardjs.com/)  [![Build Status](https://travis-ci.org/fastify/fastify-assets-compiler.svg?branch=master)](https://travis-ci.org/fastify/fastify-assets-compiler)

If you need to compile (browserify style!) your code, this plugin is for you!  
Internally it uses [bankai](https://github.com/yoshuawuyts/bankai), so refer to its documentation for the options.

## Install
```
npm i fastify-assets-compiler --save
```

## Usage
Simply require this plugin, pass the entry file and you are done!
```js
const fastify = require('fastify')()

fastify.register(require('fastify-assets-compiler'), {
  entryFile: './client.js'
})

fastify.listen(3000, err => {
  if (err) throw err
  console.log('Server listenting on localhost:', fastify.server.address().port)
})
```

## Options
- `entryFile`: Your application entry point
- `baseURL`: a custom url, default `'/'`
- `options`: the options object for bankai

## Acknowledgements

This project is kindly sponsored by:
- [nearForm](http://nearform.com)
- [LetzDoIt](http://www.letzdoitapp.com/)

## License

Licensed under [MIT](./LICENSE).
