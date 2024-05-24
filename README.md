C11emu is an emulation layer/library for the C11 (C 2011) Concurrency Support Library which has been slow to be implemented on many systems.

It provides functions like the tss_create() family of thread-local storage routines.

The code is based on @yohhoy's pure headerfile implementation as it was included in the Mesa project:
see https://gist.github.com/yohhoy/2223710

These headers are installed under `$prefix/include/c11emu/header_only`. Projects that include, for instance, `thread.h` and use the functions declared therein in a single or small number of source files can use `CFLAGS += -I/path/to/include/c11emu/header_only` if the system doesn't provide the `thread.h` headerfile itself.

Recent versions of Mesa have moved from a pure headerfile implementation to one using a library. This approach is more suitable for projects where the provided functions are called from multiple source files. It will be added in an upcoming version.

The original implementation by @yohhoy was covered by the Boost (Permissive) license; the library re-implementation by Mesa's usual MIT license.
