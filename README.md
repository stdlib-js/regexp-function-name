<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# reFunctionName

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Regular expression][regexp] to capture a function name.



<section class="usage">

## Usage

To use in Observable,

```javascript
reFunctionName = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-function-name@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var reFunctionName = require( 'path/to/vendor/umd/regexp-function-name/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/regexp-function-name@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.reFunctionName;
})();
</script>
```

#### reFunctionName()

Returns a [regular expression][regexp] to capture a `function` name.

```javascript
function beep() {
    return 'boop';
}

var RE_FUNCTION_NAME = reFunctionName();
var str = RE_FUNCTION_NAME.exec( beep.toString() )[ 1 ];
// returns 'beep'
```

#### reFunctionName.REGEXP

[Regular expression][regexp] to capture a `function` name.

<!-- eslint-disable stdlib/no-builtin-math -->

```javascript
var str = reFunctionName.REGEXP.exec( Math.sqrt.toString() )[ 1 ];
// returns 'sqrt'
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint-disable func-names, no-restricted-syntax, no-empty-function, stdlib/no-builtin-math -->

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/array-int8@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/regexp-function-name@umd/browser.js"></script>
<script type="text/javascript">
(function () {
var RE_FUNCTION_NAME = reFunctionName();

function fname( fcn ) {
    return RE_FUNCTION_NAME.exec( fcn.toString() )[ 1 ];
}

var f = fname( Math.sqrt );
// returns 'sqrt'

f = fname( Int8Array );
// returns 'Int8Array'

f = fname( Object.prototype.toString );
// returns 'toString'

f = fname( function () {} );
// returns ''

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/utils-function-name`][@stdlib/utils/function-name]</span><span class="delimiter">: </span><span class="description">determine a function's name.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-function-name.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-function-name

[test-image]: https://github.com/stdlib-js/regexp-function-name/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/regexp-function-name/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-function-name/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-function-name?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-function-name.svg
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-function-name/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/regexp-function-name/tree/deno
[umd-url]: https://github.com/stdlib-js/regexp-function-name/tree/umd
[esm-url]: https://github.com/stdlib-js/regexp-function-name/tree/esm
[branches-url]: https://github.com/stdlib-js/regexp-function-name/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-function-name/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

<!-- <related-links> -->

[@stdlib/utils/function-name]: https://github.com/stdlib-js/utils-function-name/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
