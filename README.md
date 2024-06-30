# Safe Rust wrappers for the services in the [ESP IDF SDK]

## Highlights

* Supports almost all ESP IDF services: timers, event loop, Wifi, Ethernet, HTTP client & server, MQTT, WS, NVS, OTA, etc.
* Implements the traits of [embedded-svc](https://github.com/esp-rs/embedded-svc)
* Blocking and `async` mode for each service (`async` support where feasible)
* Re-exports `esp-idf-hal` and `esp-idf-sys` as `esp_idf_svc::hal` and `esp_idf_svc::sys`. You only need to depend on `esp_idf_svc` to get everything you need

**You might want to also check out the ESP IDF [Drivers](https://github.com/esp-rs/esp-idf-hal) wrappers, and the raw bindings to ESP IDF in the [esp-idf-sys](https://github.com/esp-rs/esp-idf-sys) crate!**

## Build Prerequisites

Follow the [Prerequisites](https://github.com/esp-rs/esp-idf-template#prerequisites) section in the `esp-idf-template` crate.

## Examples

The examples could be built and flashed conveniently with [`cargo-espflash`](https://github.com/esp-rs/espflash/). To run e.g. `wifi` on an e.g. ESP32-C3:
(Swap the Rust target and example name with the target corresponding for your ESP32 MCU and with the example you would like to build)

with `cargo-espflash`:
```sh
$ MCU=esp32c3 cargo espflash flash --target riscv32imc-esp-espidf --example wifi --monitor
```

| MCU | "--target" |
| --- | ------ |
| esp32c2 | riscv32imc-esp-espidf |
| esp32c3| riscv32imc-esp-espidf |
| esp32c6| riscv32imac-esp-espidf |
| esp32h2 | riscv32imac-esp-espidf |
| esp32p4 | riscv32imafc-esp-espidf |
| esp32 | xtensa-esp32-espidf |
| esp32s2 | xtensa-esp32s2-espidf |
| esp32s3 | xtensa-esp32s3-espidf |


## Setting up a "Hello, world!" binary crate with ESP IDF

Use the [esp-idf-template](https://github.com/esp-rs/esp-idf-template) project. Everything would be arranged and built for you automatically - no need to manually clone the ESP IDF repository.

## More information

For more information, check out:
* The [Rust on ESP Book](https://esp-rs.github.io/book/)
* The [ESP Embedded Training](https://github.com/esp-rs/espressif-trainings)
* The [esp-idf-template](https://github.com/esp-rs/esp-idf-template) project
* The [embedded-svc](https://github.com/esp-rs/embedded-svc) project
* The [esp-idf-hal](https://github.com/esp-rs/esp-idf-hal) project
* The [embedded-hal](https://github.com/rust-embedded/embedded-hal) project
* The [esp-idf-sys](https://github.com/esp-rs/esp-idf-sys) project
* The [Rust for Xtensa toolchain](https://github.com/esp-rs/rust-build)
* The [Rust-with-STD demo](https://github.com/ivmarkov/rust-esp32-std-demo) project
