# Micron CXL CLI


MXCLI is a command-line application and a front-end to MCXL (Micron CXL Library).

It has two modes of operation:
* Interactive CLI.
* Classic argument-based CLI.[^1]

## Features

CXL Features:
* Access CXL Registers.
* Device management using CXL spec commands:
    * CXL.io over RAW IOCTL or Memory Mapped Register access.
    * MCTP/SMBUS [^2]
    * UART console [^3]

Other Features:
  * Access PCIe Registers.

## Prerequisites

* Linux Distribution with CXL-enabled kernel (e.g. Ubuntu 22.04, Fedora 36, CentOS 8 and REHL 9)[^4]
* The following system executables: `pci-utils`
    * Installable by package managers `yum/apt install pci-utils`
* GLIBC 2.28+ [^5]
* Root access (for sysfs R/W)

## Installation Notes

* Executable distributions are self-contained and ready to be executed.
* Optionally ensure execution mode is enabled by `chmod +x mxcli_YYYY.MM.DD`
* Launch by `./mxcli_YYYY.MM.DD` for interactive CLI or `./mxcli_YYYY.MM.DD --help` for classic mode.


Footnotes
[^1]: Limited testing done.
[^2]: Device must be connected via Aardvark setup.
[^3]: Device must be connected via UART.
[^4]: CentOS 8 os and RHEL 9 is supported from 2023.09.26 release onwards.
[^5]: Minimum GLIBC version 2.28 required.