# Ferrox

A RISC-V operating system built from scratch in Rust.

## Goals

- Build a minimal but functional OS targeting RISC-V (RV32IMAC)
- Learn OS internals hands-on: boot, memory management, processes, file systems
- Run on QEMU first, then port to custom FPGA hardware

## Status

Early development — see [milestones](https://github.com/platonoff-dev/ferrox/milestones) for progress.

## Building

Prerequisites:
- Rust nightly with `riscv32imac-unknown-none-elf` target
- QEMU (`qemu-system-riscv32`)

```sh
cargo build
```

## Project Structure

```
ferrox/
├── kernel/          # Kernel code
│   └── src/
│       └── main.rs
├── docs/            # Design notes
├── Cargo.toml       # Workspace root
└── rust-toolchain.toml
```

## License

MIT
