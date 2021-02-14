# Bare Metal

## Hardware Documentation

* [ARM Cortex-A Series Programmer's Guide for ARMv8-A](https://developer.arm.com/documentation/den0024/a/Preface)

## OS Examples / Tutorials

* [Operating System development tutorials in Rust on the Raspberry Pi]() - targets ARM v8-A in Rust. Nice source code organization.
* [Writing an OS in Rust](https://os.phil-opp.com) - targets x86. Has section on [Testing](https://os.phil-opp.com/testing/) in `#[no_std]` environments.

* [Building an Operating System for the Raspberry Pi](https://jsandler18.github.io) - C
* [rpi4-osdev](https://isometimes.github.io/rpi4-osdev/part1-bootstrapping/) - targets A72 (pi 4) in C.
* [Baking Pi](https://www.cl.cam.ac.uk/projects/raspberrypi/tutorials/os/) - targets early Raspberry Pi boards.

## Toolchain

* Compilers
  - GCC - [Official ARM version]()
  - Rust
    - Pi 0: ARM v11 `rustup target add thumbv6-none-eabi`
    - Pi 3: ARM v8 Cortex-A53 (aarch64): `rustup target add aarch64-unknown-none`
    - Pi 4: ARM v8 Cortex-A72 (aarch64): `rustup target add aarch64-unknown-none` 
  
* Emulator
  - [QEMU](https://www.qemu.org)
    - Pi 0: `qemu-system-arm  -machine raspi0 -serial stdio -kernel <path-to-kernel-binary>`
    - Pi 4: `qemu-system-aarch64  -machine raspi4 -serial stdio -kernel <path-to-kernel-binary>`

* Serial Console Interface
  - Screen
  - Serial Tools (App store)
  - Cornflake
