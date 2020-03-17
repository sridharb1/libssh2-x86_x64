# libssh2-x86_x64
Native Visual Studio solution/project files to compile in Windows
x86/x64/Release/Debug

# Background #
libssh2 uses CMake. This does not generate good solution/project
files, especially needs to be configured for x86/x64 separately. The
concept of installing it in standard locations (like /usr/local/lib)
and getting dependencies from such locations is not practiced widely
in Windows, where projects are installed into their own folders and
variables like LIB is used to link against these.

Visual Studio has a more advanced version of the same in References,
which allow one to link to a project and it automatically links to the
correct library given the current target (x86/x64/Release/Debug)
without having to specify hardcoded library paths or names.

# Installation #

  * git clone [libssh2, tested w/ v1.9.0](https://github.com/libssh2/libssh2.git)
  * Create a folder called build in this directory
  * git clone [libssh2-x86_x64](https://github.com/sridharb1/libssh2-x86_x64.git)
    to another folder
  * Copy the contents of the folder above to the build folder

# Note #

To compile libssh, you need 

  * [zlib, tested w/ v1.2.11](https://github.com/madler/zlib)
  * [OpenSSL, tested w/ v1.1.1e-DEV](https://github.com/openssl/openssl)
  * You can use my [openssl-x86_x64](https://github.com/sridharb1/openssl-x86_x64) to compile openssl on Windows.
  * [libssh, tested w/ v0.9.3](https://git.libssh.org/projects/libssh.git/)
  * You can use my [libssh-x86_x64](https://github.com/sridharb1/libssh-x86_x64.git) to compile libssh on Windows
