# ARMv6 Rust compilation image

## Background

Forked from https://github.com/mdirkse/rust_armv6

## Usage

```
# Build the docker image (in this git directory)
docker build -t rust_armv6 .

# add the compile script to the path
ln -sf "$(pwd)/cargo_build_armv6" ~/bin/cargo_build_armv6

# go the rust project root directory and execute the shell script
cargo_build_armv6
```

## Internals / Caveats

The script temporarily adds a target linker into the cargo config at `.cargo/config`. If not existing this file and folder are created.
