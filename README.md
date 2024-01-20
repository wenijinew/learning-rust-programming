# learning-rust-programming

## Cargo

- The project file is called as `Cargo.toml`(case-sensitive).
- `src/main.rs` or `src/lib.rs` should exists, otherwise `[lib]` or `[[bin]]` section should be present in `Cargo.toml`.
or it will fail to build. For example,

``` shell
error: failed to parse manifest at `/repo/wenijinew/dj/learning-rust-programming/Cargo.toml`

Caused by:
  no targets specified in the manifest
  either src/lib.rs, src/main.rs, a [lib] section, or [[bin]] section must be present
```
- `main.rs` must be compilable. When I made it empty, the build failed.

``` shell
   Compiling learning-rust-programming v0.0.1 (/repo/wenijinew/dj/learning-rust-programming)
error[E0601]: `main` function not found in crate `learning_rust_programming`
  |
  = note: consider adding a `main` function to `src/main.rs`

For more information about this error, try `rustc --explain E0601`.
error: could not compile `learning-rust-programming` due to previous error
```
