# SXD-XPath

An XML XPath library in Rust, modified to support a `no-unsafe` flag and the sxd-document-no-unsafe XML library.

[![Build Status](https://github.com/nsoiffer/sxd-xpath/workflows/Continuous%20integration/badge.svg)](https://github.com/nsoiffer/sxd-xpath/actions?query=branch%3Amaster)
[![Current Version](https://img.shields.io/crates/v/sxd-xpath-no-unsafe.svg)](https://crates.io/crates/sxd-xpath-no-unsafe)
[![Documentation](https://docs.rs/sxd-xpath-no-unsafe/badge.svg)](https://docs.rs/sxd-xpath-no-unsafe/)

## Overview

The project is broken into two crates:

1. [`document`][sxd-document] - Basic DOM manipulation and reading/writing XML from strings.
2. `xpath` - Implementation of XPath 1.0 expressions.

There are also scattered utilities for playing around at the command
line.

[sxd-document]: https://github.com/nsoiffer/sxd-document-no-unsafe/

## Goals

This project aims to offer a version of Jake Goulding's [sxd-xpath](https://crates.io/crates/sxd-xpath) library
that works with the modified version of [sxd-document](https://crates.io/crates/sxd-document).
The modified version is [sxd-document-no-unsafe](https://crates.io/crates/sxd-document-no-unsafe),
which does not contain calls to `unsafe`, for users who are constrained to avoid code containing `unsafe`.
The original library does not contain calls to `unsafe`, but needed to be modified a little to deal with differences between the two versions of sxd-document.
With default features enabled, the compiled code should match the [original project](https://github.com/shepmaster/sxd-xpath).

I have _not_ updated the documentation.

## Contributing

1. Fork it (<https://github.com/nsoiffer/sxd-xpath-no-unsafe/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Add a failing test.
4. Add code to pass the test.
5. Commit your changes (`git commit -am 'Add some feature'`)
6. Ensure tests pass.
7. Push to the branch (`git push origin my-new-feature`)
8. Create a new Pull Request

## License

Licensed under either of

* Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or https://www.apache.org/licenses/LICENSE-2.0)
* MIT license ([LICENSE-MIT](LICENSE-MIT) or https://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you shall be dual licensed as above, without any
additional terms or conditions.
