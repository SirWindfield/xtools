# xtools

[![Maintenance](https://img.shields.io/badge/maintenance-actively%20maintained-brightgreen.svg)](https://github.com/SirWindfield/xtools)
[![crates.io](https://img.shields.io/crates/v/xtools.svg)](https://crates.io/crates/xtools)
[![crates.io](https://img.shields.io/crates/d/xtools)](https://crates.io/crates/xtools)
[![Documentation](https://docs.rs/xtools/badge.svg)](https://docs.rs/xtools)
[![docs_master_badge]][docs_master_url]

> Git hooks written in Rust and delivered as a git submodule.

## Usage

Usually, I add the binary as a workspace member to a project of mine. You can register it as a git submodule as well, allowing you to keep the local copy up-to-date with the remote version. You can then setup an alias inside your `.cargo/config` folder:
```toml
xtools = "run --package xtools --bin xtools --"
```
This allows you to run the utility binary using `cargo xtools`.

## Features

`xtools` provides some utility binaries that can be used to create custom git hooks. Here is a (non-exhaustive) list:
- git:
  - check for clean workspace flow
  - various hooks, for example `pre-commit` that checks that `cargo clippy && cargo fmt -- --check` succeed without errors.
- rust:
  - clippy flow
  - rustfmt flow
  
To modify the git hooks and run custom flows, you can simply modify the source code. The hooks get compiled alongside your Rust project, which creates a natural development environment for your git hooks.  

## Current Properties

- MSRV: 1.41.0 (tested)

## License

Licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  https://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or https://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.

[docs_master_badge]: https://img.shields.io/badge/docs.rs-master-green
[docs_master_url]: https://<username>.github.io/<reponame>
