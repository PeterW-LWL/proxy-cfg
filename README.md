# proxy-cfg
[![Crates.io](https://img.shields.io/crates/v/proxy-cfg.svg)](https://crates.io/crates/proxy-cfg)
[![Documentation](https://docs.rs/proxy_cfg/badge.svg)](https://docs.rs/proxy_cfg)

A Rust library to get proxy configuration from the OS.

## Usage

```Rust
if let Ok(Some(proxy_config)) = proxy_cfg::get_proxy_config() {
    if let Some(proxy_address) = proxy_config.get_proxy_for_url(Url::parse("http://www.google.com").unwrap()) {
        // use proxy_address to connect
    }
}
```

## License

This project is provided under the terms of the Apache License 2.0 or the MIT License, at your option.

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the work by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any additional terms or conditions.
