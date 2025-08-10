# embedded-systems-lab

A starter project for learning embedded systems and all about it.


## Repository Structure

```
embedded-systems-lab/
├── apps/                     # Buildable applications (each with its own CMakeLists.txt)
│   ├── telemetry_node/       # Ethernet + FreeRTOS + lwIP example
│   │   └── src/
│   ├── can_dual_node/        # CAN bus dual-node example
│   │   └── src/
│   └── bootloader/           # Minimal bootloader project
│       └── src/
├── boards/                   # Board-specific configuration
│   ├── nucleo_f767zi/
│   │   ├── openocd/          # OpenOCD interface & target configs
│   │   └── README.md
│   ├── nucleo_h743zi2/
│   │   ├── openocd/
│   │   └── README.md
│   └── common/               # Shared board utilities
├── cmake/                    # Toolchain & common CMake modules
├── drivers/                  # Reusable peripheral drivers
├── middleware/               # FreeRTOS, lwIP, mbedTLS (as submodules or fetched)
│   ├── freertos/
│   ├── lwip/
│   └── mbedtls/
├── protocols/                # Small, reusable protocol libraries
│   ├── cobs/
│   │   ├── include/
│   │   └── src/
│   └── crc/
│       ├── include/
│       └── src/
├── scripts/                   # Flashing, formatting, helper scripts
├── tests/                     # Host (native) & on-target tests
│   ├── host/
│   └── target/
├── tools/                     # Utilities (serial, OpenOCD helpers)
│   ├── serial/
│   └── openocd/
├── docs/                      # Documentation, diagrams
├── third_party/               # External libraries
├── .github/workflows/         # CI pipelines
├── .clang-format              # Code style
├── .clang-tidy                # Static analysis rules
├── .gitignore
├── CMakeLists.txt
└── README.md
```

## Initial installments (Arch Linux)

### the script

```bash

yay -Syu --needed base-devel git cmake ninja python python-pip clang clang-tools-extras bear arm-none-eabi-gcc arm-none-eabi-binutils arm-none-eabi-newlib arm-none-eabi-gdb openocd stlink dfu-util qemu-system-arm minicom picocom cppcheck doxygen graphviz

#To make sure you got the correct access, run:
sudo usermod -aG uucp,lock $USER


```

### What they do (notes for myself)

```
base-devel              # Contains essential packages for building software, including GCC and Make.
git                     # Git is a version control system, which makes it easier for users to add, change and collaborate when writing code and files.
cmake                   # Is a software development tool that can help structure tests, packaaging, installations and more.
ninja                   # It's another build system that focusing on speed. It relies on other build systems and ninja itself does the assembling
python                  # the programming language python.
python-pip              # The package manager for python.
clang                   # Is another compiler like GCC.
clang-tools-extras      # Extra tools for clang
bear                    # A tool to generate compilation database for Clang tooling
arm-none-eabi-gcc       # The GCC compiler for embedded (in this project atleast)
arm-none-eabi-binutils  # a collection of tools for working with binary and object files when working on embeeded system. 
arm-none-eabi-newlib    # A C standard library implementation intended for use on embedded systems (ARM bare metal)
arm-none-eabi-gdb       # GNU debugger for ARM/Embedded systems.
openocd                 # Debugging, in-system programming and boundary-scan testing for embedded target devices
stlink                  # a toolset for programming and debugging STM32 boards and devices.
dfu-util                # Is often used to update firmware of devices.
qemu-system-arm         # QEMU system emulator for ARM.
minicom                 # A free source code that is a communication program.
picocom                 # A minimal terminal emulation program.
cppcheck                # A tool for static C/C++ code analysis.
doxygen                 # Documentation system for various programming languages
graphviz                # A rich set of graph drawing tools.


```
