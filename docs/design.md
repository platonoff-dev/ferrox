# Ferrox Design Notes

## Architecture

- **Target**: RISC-V RV32IMAC (32-bit, integer + multiply + atomic + compressed)
- **Platform**: QEMU `virt` machine initially, custom FPGA later
- **Language**: Rust (`no_std`), minimal assembly for boot and trap entry

## Inspiration

- [xv6-riscv](https://github.com/mit-pdos/xv6-riscv) — MIT teaching OS
- [Writing an OS in Rust](https://os.phil-opp.com/) — Philipp Oppermann's blog series
- [RISC-V Privileged Specification](https://riscv.org/specifications/privileged-isa/)
- The RISC-V Reader (Patterson & Waterman)

## Key Design Decisions

- **Sv32** virtual memory (2-level page tables, 32-bit virtual addresses)
- **Monolithic kernel** — simpler to build and debug for learning purposes
- **Preemptive scheduling** with timer interrupts
- **Simple file system** — custom or FAT-based, stored on SD card via SPI
