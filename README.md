# bif.ksy
Kaitai Struct for Roku's Base Index Frames (BIF) image archive format

## What is Kaitai Struct?

A declarative language-neutral binary parsing language. Read about it [here](https://kaitai.io/#what-is-it).

## How to use

Use the `kaitai-struct-compiler` tool to compile to practically any language for usage. Check out the user guide for how to do that [here](https://doc.kaitai.io/user_guide.html#ksc).

## Fields

This was based off of Roku's [BIF File Specification](https://developer.roku.com/docs/developer-program/media-playback/trick-mode/bif-file-creation.md#bif-file-specification).

Each BIF file (according to this struct) will have a Header and Images, and each field is well-documented within the KSY and the Roku specification.

### Header:
- Magic
- Version
- Number of images
- Timestamp multiplier

### Images (array, size is number of images in Header):
- Timestamp
- Offset
- JPEG binary data
