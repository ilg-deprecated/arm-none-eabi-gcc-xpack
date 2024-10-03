## DEPRECATED! 

Use https://github.com/xpack-dev-tools/arm-none-eabi-gcc-xpack!

---

[![npm (scoped)](https://img.shields.io/npm/v/@gnu-mcu-eclipse/arm-none-eabi-gcc.svg)](https://www.npmjs.com/package/@gnu-mcu-eclipse/arm-none-eabi-gcc) 
[![npm](https://img.shields.io/npm/dw/@gnu-mcu-eclipse/arm-none-eabi-gcc.svg)](https://www.npmjs.com/package/@gnu-mcu-eclipse/arm-none-eabi-gcc/) 
[![npm](https://img.shields.io/npm/dt/@gnu-mcu-eclipse/arm-none-eabi-gcc.svg)](https://www.npmjs.com/package/@gnu-mcu-eclipse/arm-none-eabi-gcc/)

## The GNU MCU Eclipse ARM Embedded GCC binary xPack

This binary xPack installs the platform specific binaries for
[GNU MCU Eclipse ARM Embedded GCC](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc).

The source files of the xPack project are publicly available from 
[GitHub](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc-xpack).

## How to use

This section is intended for developers who plan to use the 
ARM Embedded GCC toolchain.

### Prerequisites

The only requirement is a recent 
`xpm`, which is a portable 
[Node.js](https://nodejs.org) command line application. To install it,
follow the instructions from the 
[`xpm`](https://www.npmjs.com/package/xpm) page.

### Easy install

The xPack is available as 
[`@gnu-mcu-eclipse/arm-none-eabi-gcc`](https://www.npmjs.com/package/@gnu-mcu-eclipse/arm-none-eabi-gcc) 
from the public `npmjs.com` repository; with `xpm` available, installing 
the latest version of the package is quite easy:

```console
$ npm update --global xpm
$ xpm install --global @gnu-mcu-eclipse/arm-none-eabi-gcc
```

Global xPacks are always installed in the user home folder, even on GNU/Linux 
or macOS, and do not require `sudo`.

The GNU MCU Eclipse plug-ins automatically identify binaries installed with
`xpm` and provide a convenient method to manage paths.

To remove the installed xPack, the command is similar:

```console
$ xpm uninstall --global @gnu-mcu-eclipse/arm-none-eabi-gcc
```

(Note: not yet implemented. As a temporary workaround, simply remove the 
`xPacks/@gnu-mcu-eclipse/arm-none-eabi-gcc` folder, or the versions subfolders.)

## Developer info

### The xPack git repo

The few xPack source files are available from GitHub:

```console
$ git clone https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc-xpack.git arm-none-eabi-gcc-xpack.git
```

### Binary files

The binaries are not stored on the `npmjs.com` server, but are downloaded from  
the [releases](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases) 
section of the `gnu-mcu-eclipse/arm-none-eabi-gcc` GitHub project.

## Maintainer info

### How to publish

* open [releases](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases) 
and select the latest release
* update the `baseUrl:` with the file URLs (including the tag/version)
* from the blog post, copy the SHA & file names
* commit all changes, use a message like `package.json: update urls for v7.2.0-1.2 release`
* update `CHANGELOG.md`; commit with a message like _CHANGELOG: prepare v7.2.0-1.2.1_
* `npm version 7.2.0-1.2.1`
* push all changes to GitHub
* `npm publish`

Multiple xPack releases referring to the same GitHub release have an extra 
digit in the version field, like `7.2.0-1.2.3`.

## License

The original content is released under the 
[MIT License](https://opensource.org/licenses/MIT), with all rights 
reserved to [Liviu Ionescu](https://github.com/ilg-ul).

The binary distributions include several open-source components; the
corresponding licenses are available in the `.content/gnu-mcu-eclipse/licenses`
folder of the installed package.
