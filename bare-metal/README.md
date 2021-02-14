# Bare Metal

## OS Examples / Tutorials

* [Writing an OS in Rust](https://os.phil-opp.com) - targets x86.
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
