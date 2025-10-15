# ZX Spectrum Floppy Disk Images

This repository contains disk images for ZX Spectrum floppy disk drives. These images are prepared for use with the Gotek floppy emulator running [FlashFloppy](https://github.com/keirf/flashfloppy "FlashFloppy") firmware. Additionally, the disk images can be written to actual floppy disks for use with original ZX Spectrum disk drives.

## Greaseweazle Device

For users of the [Greaseweazle](https://github.com/keirf/greaseweazle "Greaseweazle") device, this repository provides disk images compatible with built-in disk format definitions, simplifying the process of writing and creating images.

#### The .diskdef disk definitions from this repository are no longer needed, as the [Greaseweazle](https://github.com/keirf/greaseweazle "Greaseweazle") software has supported them natively since version 1.22.
## How to Use

### Opus Discovery

#### Writing a `.opd` Disk Image to Floppy

1. Rename the file extension from `.opd` to `.img`.
2. Run the following command to write the image:

    ```sh
    gw write --format zx.opus.ss40 example.img
    ```

#### Creating a Disk Image

1. Run the following command to read and create a disk image:

    ```sh
    gw read --format zx.opus.ss40 example.img
    ```

2. Rename the file extension from `.img` to `.opd`.

### MGT +D

#### Writing a `.mgt` Disk Image to Floppy

1. Run the following command to write the image:

    ```sh
    gw write --format zx.plusd.ds80 example.mgt
    ```

#### Creating a Disk Image

1. Run the following command to read and create a disk image:

    ```sh
    gw read --format zx.plusd.ds80 example.mgt
    ```

### +3DOS

#### Writing a `.dsk` Disk Image to Floppy

1. Run the following command to write the image:

    ```sh
    gw write example.dsk
    ```

#### Creating a Disk Image

1. Run the following command to read and create a disk image:

    ```sh
    gw read --format zx.3dos.ss40 example.edsk
    ```

2. Rename the file extension from `.edsk` to `.dsk`.

### Betadisk TR-DOS

#### Writing a `.trd` Disk Image to Floppy

1. Run the following command to write the image:

    ```sh
    gw write --format zx.trdos.ds80 example.trd
    ```

#### Creating a Disk Image

1. Run the following command to read and create a disk image:

    ```sh
    gw read --format zx.trdos.ds80 example.trd
    ```

## Supported Disk Formats

This repository supports the following disk formats:

- **Betadisk TR-DOS**: `zx.trdos.ds80`
- **Quorum CP/M-80**: `zx.quorum.ds80`
- **Didaktik D80**: `zx.d80.ds80`
- **Timex FDD 3000**: `zx.fdd3000.ss40`, `zx.fdd3000.ds80`
- **Kempston Disk Interface**: `zx.kempston.ss40`, `zx.kempston.ds80`
- **MGT +D**: `zx.plusd.ds80`
- **Opus Discovery**: `zx.opus.ss40`, `zx.opus.ds80`
- **ZX Spectrum +3DOS**: `zx.3dos.ss40`, `zx.3dos.ds80`
- **Rocky Gush**: `zx.rocky.ss40`, `zx.rocky.ds80`
- **Turbodrive**: `zx.turbodrive.ds40`, `zx.turbodrive.ds80`
- **Watford SPDOS**: `zx.watford.ss40`, `zx.watford.ds80`

## System Requirements

Some floppy disk interfaces may require a system on disk to function correctly. The disk images in this repository include the necessary system files to ensure proper operation.
