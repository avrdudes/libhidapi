# HIDAPI library for Windows

This library is a fork of [hidapi](https://github.com/libusb/hidapi).

The design objective of this library is to provide a better
out-of-the-box experience for [AVRDUDE](https://github.com/avrdudes/avrdude) Windows users.

This library only supports a subset of the original implementation.
The intend is not to provide a general purpose implementation,
but to satisfy the usage scenarios of AVRDUDE.

This library supports only **Microsoft Visual C/C++**,
as used in the **msvc** job of the [AVRDUDE build action](https://github.com/avrdudes/avrdude/blob/main/.github/workflows/build.yml).

The latest version of libhidapi for Windows can be found here:\
<https://github.com/avrdudes/libhidapi>

The original README of hidapi can be found here: [README-old.md](./README-old.md).

## Notable Changes

Currently, the Windows related code does no longer required any patches,
so it is identical with the upstream version.

In the long term, the Windows version of AVRDUDE should use the official
hidapi library, and this library will be deprecated.
