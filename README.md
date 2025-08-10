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

