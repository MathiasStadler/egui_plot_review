# path of MY steps to explore this

## start of project
<!-- keep the format -->
```bash <!-- markdownlint-disable-line code-block-style -->
Wed Sep 10 08:39:19 PM CEST 2025
```
<!-- keep the format -->
## Show active toolchain
<!-- keep the format -->
```bash <!-- markdownlint-disable-line code-block-style -->
Wed Sep 10 08:39:19 PM CEST 2025
```
<!-- keep the format -->
## Show which toolchain is active
<!-- keep the format -->
```bash <!-- markdownlint-disable-line code-block-style -->
rustup show
# or better
rustup show |sed -n '/active toolchain/,/^$/p'

## output
active toolchain
----------------
name: 1.85-x86_64-unknown-linux-gnu
active because: overridden by '/var/trapapa_workspce_codium/egui_plot/rust-toolchain'
installed targets:
  wasm32-unknown-unknown
  x86_64-unknown-linux-gnu

:bangbang: Please check and remove
cargo tree --depth 1|sed -n '1!p'

```
<!-- keep the format -->
## Rust stable version
<!-- keep the format -->
```bash <!-- markdownlint-disable-line code-block-style -->
https://releases.rs
```
<!-- -->
## Change to latest stable version
<!-- -->
```bash <!-- markdownlint-disable-line code-block-style -->
rustup override set stable-x86_64-unknown-linux-gnu
cargo clean
# test again which toolchain is active
rustup show |sed -n '/active toolchain/,/^$/p'
## be save and set again
export RUSTC_WRAPPER=sccache
cargo build
```

## Update rust , toolchain and crates
