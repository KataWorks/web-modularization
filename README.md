# web-modularization

* Figure out the sequence
  * a `index.html` with a lot of `<script>` tags, figure out the right sequence to load all the scripts correctly.
* Implement `define`
  * make all the scripts wrapped with `define` function and import dependencies by `require` as the parameter of `define`.
  * implement `define` to load all the scripts correctly.
* Asynchronize `require`
  * remove all the `<script>` tags and left only one for `require.js` to setup the main entry  `app.js`.
  * implement `define` in `require.js` to import dependencies by adding `<script>` tag asynchronously.
* Get together
  * implement a Node.js program `webpack.js` to glue all the scripts together as one script file.
* Rip the wrapper
  * remove all the invoking of `define` function but left callback body, and replace return statement with re-assigning value for `module.exports`.
  * implement `webpack.js` to load all the wrapper-ripped scripts correctly.
* Configurable

## Reference

* [Initial version of `webpack`](https://github.com/webpack/webpack/tree/2e1460036c5349951da86c582006c7787c56c543)
* [sokra](https://github.com/sokra)
* [`eval` context](http://www.ecma-international.org/ecma-262/5.1/#sec-10.4.2)