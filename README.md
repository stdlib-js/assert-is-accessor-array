<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

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

# isAccessorArray

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Test if a value is an array-like object supporting the accessor (get/set) protocol.

<section class="intro">

An accessor array is defined as either an [`Array`][mdn-array], [`Typed Array`][mdn-typed-array], or an array-like [`Object`][mdn-object] (excluding `strings` and `functions`) having `get` and `set` methods for accessing array elements.

</section>

<!-- ./intro -->



<section class="usage">

## Usage

```javascript
import isAccessorArray from 'https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-accessor-array@esm/index.mjs';
```

#### isAccessorArray( value )

Tests if a value is an array-like object supporting the accessor (get/set) protocol.

```javascript
import Complex128Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-complex128@esm/index.mjs';
import Complex128 from 'https://cdn.jsdelivr.net/gh/stdlib-js/complex-float64@esm/index.mjs';

// Create a new complex number array:
var arr = new Complex128Array( 10 );

// Retrieve a complex number element:
var z = arr.get( 0 );
// returns <Complex128>

// Set a complex number element:
arr.set( new Complex128( 1.0, 1.0 ), 0 );

// ...

// Check whether an array is an accessor array:
var bool = isAccessorArray( arr );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint-disable object-curly-newline -->

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import Int8Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-int8@esm/index.mjs';
import Uint8Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-uint8@esm/index.mjs';
import Uint8ClampedArray from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-uint8c@esm/index.mjs';
import Int16Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-int16@esm/index.mjs';
import Uint16Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-uint16@esm/index.mjs';
import Int32Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-int32@esm/index.mjs';
import Uint32Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-uint32@esm/index.mjs';
import Float32Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-float32@esm/index.mjs';
import Float64Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-float64@esm/index.mjs';
import Complex128Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-complex128@esm/index.mjs';
import Complex64Array from 'https://cdn.jsdelivr.net/gh/stdlib-js/array-complex64@esm/index.mjs';
import isAccessorArray from 'https://cdn.jsdelivr.net/gh/stdlib-js/assert-is-accessor-array@esm/index.mjs';

var bool = isAccessorArray( new Complex128Array( 10 ) );
// returns true

bool = isAccessorArray( new Complex64Array( 10 ) );
// returns true

bool = isAccessorArray( [] );
// returns false

bool = isAccessorArray( new Float64Array( 10 ) );
// returns false

bool = isAccessorArray( new Float32Array( 10 ) );
// returns false

bool = isAccessorArray( new Int32Array( 10 ) );
// returns false

bool = isAccessorArray( new Uint32Array( 10 ) );
// returns false

bool = isAccessorArray( new Int16Array( 10 ) );
// returns false

bool = isAccessorArray( new Uint16Array( 10 ) );
// returns false

bool = isAccessorArray( new Int8Array( 10 ) );
// returns false

bool = isAccessorArray( new Uint8Array( 10 ) );
// returns false

bool = isAccessorArray( new Uint8ClampedArray( 10 ) );
// returns false

bool = isAccessorArray( { 'length': 0 } );
// returns false

bool = isAccessorArray( {} );
// returns false

bool = isAccessorArray( 'beep' );
// returns false

bool = isAccessorArray( isAccessorArray );
// returns false

bool = isAccessorArray( null );
// returns false

bool = isAccessorArray( void 0 );
// returns false

bool = isAccessorArray( 3.14 );
// returns false

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/assert-is-accessor-array.svg
[npm-url]: https://npmjs.org/package/@stdlib/assert-is-accessor-array

[test-image]: https://github.com/stdlib-js/assert-is-accessor-array/actions/workflows/test.yml/badge.svg?branch=v0.0.1
[test-url]: https://github.com/stdlib-js/assert-is-accessor-array/actions/workflows/test.yml?query=branch:v0.0.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/assert-is-accessor-array/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/assert-is-accessor-array?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/assert-is-accessor-array.svg
[dependencies-url]: https://david-dm.org/stdlib-js/assert-is-accessor-array/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/assert-is-accessor-array/tree/deno
[umd-url]: https://github.com/stdlib-js/assert-is-accessor-array/tree/umd
[esm-url]: https://github.com/stdlib-js/assert-is-accessor-array/tree/esm
[branches-url]: https://github.com/stdlib-js/assert-is-accessor-array/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/assert-is-accessor-array/main/LICENSE

[mdn-array]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array

[mdn-typed-array]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray

[mdn-object]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
