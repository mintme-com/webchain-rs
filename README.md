<p align="center">
  <h2 align="center">Webchain Vault</a></h3>
  <p align="center">Secure account management for Webchain Network</a></p>
  <p align="center">
    <a href="LICENSE"><img alt="Software License" src="https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square&maxAge=2592000"></a>
  </p>
</p>

---



```
NOTE:

An offline wallet, also known as cold storage, provides the highest level of security for savings.
It involves storing a wallet in a secured place that is not connected to the network (air-gapped).
When done properly, it can offer a very good protection against computer vulnerabilities.
```

Distributed as a Rust crate or can be embedded via foreign function interface (FFI).

For minimalistic CLI tool refer to [Webchain-cli](https://github.com/webchain-network/webchain-cli), or if you looking for a fully-featured UI online wallet, take a look at our [Webchain Network Wallet](https://github.com/webchain-network/webchain-wallet)


## Features

### General

* [x] Accounts
* [x] Transactions signing
* [x] Smart contracts (ABI)
* [ ] C interface (ABI)

## Installation

Ensure you have these dependencies installed:

```
openssl pkgconfig rustc cargo clang
```

`cargo` and `rustc` should be at least versions 0.18 and 1.17 respectively.

If you use [Nix](http://nixos.org/nix) you may execute the `nix-shell` command in your cloned repository and all dependencies will be made available in your environment automatically.

## Examples

```
extern crate emerald_core as emerald;

use std::net::SocketAddr;

fn main() {
    let addr = "127.0.0.1:1920"
        .parse::<SocketAddr>()
        .expect("Expect to parse address");

    emerald::start(&addr, None, None);
}
```

## References

 [JSON-RPC API](docs/api.md)
 
## Contact
 Chat with us via [Gitter](https://gitter.im/webchain-network/public)

## License

Apache 2.0
