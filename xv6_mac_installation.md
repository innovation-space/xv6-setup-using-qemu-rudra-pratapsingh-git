# How to Install and Set Up QEMU and xv6 on macOS

Follow these steps to set up the RISC-V cross-compilation environment and run the MIT xv6 operating system on macOS:

1. **Launch Terminal**: Open the **Terminal** application on your Mac.
2. **Update Homebrew**: Refresh your Homebrew package definitions to ensure you get the latest packages:
   ```bash
   brew update
   ```
3. **Install QEMU and RISC-V Compiler**: Install QEMU emulator and the `riscv64-elf-gcc` cross-compiler toolchain:
   ```bash
   brew install qemu riscv64-elf-gcc
   ```
4. **Verify Toolchain Installation**: Check that the RISC-V cross-compiler is working and properly installed:
   ```bash
   riscv64-elf-gcc --version
   ```
5. **Clone xv6-riscv Repository**: Fetch the official MIT xv6-riscv source code from GitHub:
   ```bash
   git clone https://github.com/mit-pdos/xv6-riscv.git
   ```
6. **Navigate to Source Directory**: Change your working directory into the cloned project folder:
   ```bash
   cd xv6-riscv
   ```
7. **Build and Run xv6**: Compile the kernel code and launch xv6 inside the QEMU emulator:
   ```bash
   make qemu
   ```
8. **Exit QEMU Emulator**: Quit the QEMU environment and return to your Mac terminal prompt by pressing `Ctrl+A` followed by `X`.
