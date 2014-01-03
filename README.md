makefiles
=========

(Currently only a single Makefile; more in the future.)

A Makefile for building single-target C++ projects.

Features
--------

- Set your executable name and source directories. That's all.
- No need to track dependencies in the `Makefile`.
- Incremental compilation works with source and header file changes.
- Compile mixed C++ / C projects.
- Compile and link options are easily configurable.
- Compact and clean.

Requirements
------------

`Makefile` requires GNU Make and the GCC toolchain (or any other that
supports `-M`-like dependency generation). It may be possible to use
`Makefile` in other environments with little or no modificaiton.

Usage
-----

Add `Makefile` to your project and change `TARGET` and `SRC_DIRS` to
match your project. Optionally adjust the settings in the "Compilation
and linking" section.


Example
-------

For a project called "Calculator" with subdirectories "src/" and "src/util",
modify `Makefile` as follows:

``` Makefile
#---------- Basic settings  ----------#
TARGET   = Calculator
SRC_DIRS = src src/util
```

To use C++11, enable all warnings and aggressive optimizations, and link
to the math library, you may also have something like this:

``` Makefile
#---------- Compilation and linking ----------#
CXX        = g++
SRC_SUFFIX = .cc .c
CXX_LANG   = -Wall -Wextra -pedantic -Wfatal-errors -std=c++11
CXX_OPT    = -O3 -march=native -flto
INC_DIRS   = -Isrc
LINK_FLAGS = -lm
```
