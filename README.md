Smart Makefiles
===============

Makefiles for auto-building single-target C/C++ projects.
Drop it in your project and never worry about build dependencies again!

Features
--------

- Set your executable name and source directory. That's all.
- No need to track dependencies in the `Makefile`.
- Incremental compilation works with source and header file changes.
- Compile C++, C, or mixed projects.
- Compile and link options are easily configurable.
- Compact and clean.

Requirements
------------

`Makefile` requires GNU Make and the GCC toolchain (or any other that
supports `-M`-like dependency generation). It may be possible to use
`Makefile` in other environments with little or no modificaiton.

Versions
--------

- `Makefile_plain` is the basic version which is simple and extremely compact.
- `Makefile_gtest` adds support for unit testing with the googletest framework (recommended).

Usage
-----

Add `Makefile_gtest` (or `Makefile_plain`) to your project and rename it to `Makefile`.
Change `PROGRAM_NAME` and `SRC_BASE` to match your project. Optionally adjust the settings
in the "Compilation and linking" section to match your needs.

