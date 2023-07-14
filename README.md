# Micron CXL CLI


MXCLI is a command-line application and a front-end to MCXL (Micron CXL Library).

It has two modes of operation:
* Interactive CLI
* Classic argument-based CLI [^1]

## Features

CXL Features:
* Access CXL Registers
* Device management using CXL spec commands:
    * CXL.io over RAW IOCTL or Memory Mapped Register access
    * MCTP/SMBUS [^2]
    * UART console [^2]

Other Features:
  * Access PCIe Registers

## Prerequisites

* Linux Distribution with CXL-enabled kernel (e.g. Ubuntu 22.04 or Fedora 36)
* The following system executables: `pci-utils`
    * Installable by package managers `yum/apt install pci-utils`
* GLIBC 2.35+
* Root access (for sysfs R/W)

## Installation Notes

* Executable distributions are self-contained and ready to be executed
* Optionally ensure execution mode is enabled by `chmod +x mxcli`
* Launch by `./mxcli` for interactive CLI or `./mxcli --help` for classic mode


Footnotes
[^1]: Limited testing done
[^2]: Select platforms only