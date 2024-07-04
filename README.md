# ZX Spectrum Floppy Disk Images

This repository contains disk images for ZX Spectrum floppy disk drives. These images are prepared for use with the Gotek floppy emulator running [FlashFloppy](https://github.com/keirf/flashfloppy "FlashFloppy") firmware.

## Greaseweazle Device

For those using the [Greaseweazle](https://github.com/keirf/greaseweazle "Greaseweazle") device, disk definition (diskdef) files are included in this repository. These files contain the disk definitions needed to create proper disk images.

## How to use

### Opus Discovery

#### Writing a .opd disk image to floppy

1. Place the `diskdefs.cfg` file into the main Greaseweazle directory.
2. Change the filename extension from `.opd` to `.img`.
3. Run the following command to write the image:

    ```sh
    gw write --diskdefs diskdefs.cfg --format zx.opus.sssd example.img
    ```

#### Creating a Disk Image

1. Run the following command to read and create a disk image:

    ```sh
    gw read --diskdefs diskdefs.cfg --format zx.opus.sssd example.img
    ```

2. Change the filename extension from `.img` to `.opd`.

### MGT +D

#### Writing a .mgt disk image to floppy

1. Place the `diskdefs.cfg` file into the main Greaseweazle directory.
2. Run the following command to write the image:

    ```sh
    gw write --diskdefs diskdefs.cfg --format zx.plusd.dsdd example.mgt
    ```

#### Creating a Disk Image

1. Run the following command to read and create a disk image:

    ```sh
    gw read --diskdefs diskdefs.cfg --format zx.plusd.dsdd example.mgt
    ```

## System Requirements

Some floppy disk interfaces may require a system on disk to function correctly. The disk images in this repository include the necessary system files to ensure proper operation.
