# My OS Kernel Workspace

This project is a simple operating system kernel designed for the ARM architecture. It includes a bootloader and various kernel components such as memory management, interrupt handling, and device drivers.

## Project Structure

```
my_os_kernel_workspace
├── bootloader
│   └── boot.asm          # Assembly code for the bootloader
├── kernel
│   ├── arch
│   │   └── arm
│   │       ├── gdt.c     # Global Descriptor Table implementation
│   │       ├── gdt.h     # GDT header file
│   │       ├── idt.c     # Interrupt Descriptor Table implementation
│   │       ├── idt.h     # IDT header file
│   │       ├── isr.c     # Interrupt Service Routines implementation
│   │       ├── isr.h     # ISR header file
│   │       ├── paging.c   # Paging implementation
│   │       ├── paging.h   # Paging header file
│   │       ├── port.c     # Hardware port access functions
│   │       └── port.h     # Port header file
│   ├── drivers
│   │   ├── keyboard.c     # Keyboard driver implementation
│   │   └── keyboard.h     # Keyboard driver header file
│   ├── fs
│   │   ├── fs.c           # File system implementation
│   │   └── fs.h           # File system header file
│   ├── include
│   │   ├── stdio.h        # Standard I/O functions
│   │   ├── stdlib.h       # Standard library functions
│   │   ├── string.h       # String manipulation functions
│   │   └── types.h        # Type definitions
│   ├── kernel.c           # Main kernel entry point
│   ├── kernel.ld          # Linker script for the kernel
│   └── Makefile           # Build instructions for the kernel
├── .vscode
│   ├── settings.json       # VS Code settings
│   └── tasks.json          # VS Code tasks
├── Makefile                # Overall project build instructions
└── README.md               # Project documentation
```

## Setup Instructions

1. Clone the repository:
   ```
   git clone <repository-url>
   cd my_os_kernel_workspace
   ```

2. Build the project:
   ```
   make
   ```

3. Run the kernel in an emulator (e.g., QEMU):
   ```
   qemu-system-arm -kernel path/to/kernel.img
   ```

## Usage

This kernel can be extended by adding new drivers, file systems, or other components. Refer to the individual files for implementation details and usage instructions.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for any suggestions or improvements.