# Substrate nannou template

![](nannou-substrate.png)

[**nannou**](https://nannou.cc/) is open-source creative-coding toolkit for Rust.

This project is a template for creating Non-Fungible in-browser experiences via Substrate + nannou.

The idea is to compile nannou sketches into wasm. The wasm blob is then uploaded into IPFS and the CID is included into
the metadata of an NFT to be minted on a Substrate chain.

A `webpack`-based dApp fetches this metadata from the Substrate chain and displays it as an in-browser experience.

## nannou sketch as NFT

The `nannou` directory contains the nannou sketch. It is the Rust codebase that generates the wasm-based Non-Fungible
in-browser experience.

Please refer to the [official nannou guide](https://guide.nannou.cc/) to learn more about sketches.
```
└── nannou
    ├── Cargo.toml
    └── src
        ├── lib.rs
        └── sketch.rs   <- entrypoint for nannou sketch
```

The template provides a sketch taken from nannou's [Nature of Code](https://github.com/nannou-org/nannou/tree/master/nature_of_code) example sketches.

You should build your sketch via:
```shell
$ wasm-pack build --target bundler
```

Then, upload and pin the contents of `pkg` to IPFS.

### minting the NFT

xxx

json metadata

xxx

## dApp

The `dapp` directory contains a dApp that fetches the metadata from the Substrate chain and displays it as an in-browser experience.

## References

This project is heavily inspired by [`github.com/tomoyanonymous/nannou-web-template`](https://github.com/tomoyanonymous/nannou-web-template)