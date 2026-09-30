# ROS

A hobby x86 kernel written in C, featuring basic memory management, interrupt handling, VGA/TTY output, keyboard input, and a minimal libc.

## Implemented Features

- **x86 32-bit Protected Mode**
  - GDT / IDT
  - 8259 PIC remapping

- **Memory Management**
  - Basic physical memory allocator (kheap)
  - Parsing the memory map provided by a Multiboot bootloader

- **Interrupts**
  - CPU exception handling
  - Hardware IRQs (including keyboard IRQ)

- **VGA / TTY**
  - VGA text-mode output
  - Basic TTY support

- **Keyboard**
  - PS/2 keyboard driver
  - Scancode-to-key input handling

- **User Mode**
  - Basic ring 3 transition

- **Minimal libc**
  - String operations
  - Memory operations



## Project Layout

```text
ROS/
├── kernel/       # Kernel source code
├── libc/         # Minimal C library
├── scripts/      # Build and helper scripts
├── Makefile
└── configure.sh
```

## Building

**Prerequisites:** cross-compiler (`i686-elf-gcc`)

```bash
chmod +x configure.sh
./configure.sh
make
make run
```

> `make run` requires QEMU.

## Toolchain
* i686: https://github.com/lordmilko/i686-elf-tools

## Contributing

Educational project. Fork, create a branch, and submit a PR.

## License

See [`LICENSE`](LICENSE).
