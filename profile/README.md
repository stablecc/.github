## Stable Cloud Computing

The goals of the scclib system are to allow developers to build and run software on [Linux](https://www.linux.org/),
or any POSIX-compatible environment, with minimal dependencies on OS packages, and a simplified build system.

The goals of the library are to provide modular support for the following:
* Systems software primitives, including events, polling, and stream pipelines
* IPv6 networking
* Public Key Infrastructure (PKI) support, including RSA and Elliptical Curve (EC) public keys, and H.509 certificates
* Transport Layer Security (TLS)
* HTTP client and server, including support for required services such as zlib compression

The library and support repositories can be built easily and efficiently on cloud servers and other virtual machines, embedded devices, and in docker containers.

All scc repositories depend on the [scclib library](https://github.com/stablecc/scclib) a foundational library which requires:
* [Linux](https://www.linux.org/), or a POSIX-compatible system such as [cygwin](https://www.cygwin.com/).
* [GCC](https://gcc.gnu.org), with support for Standard C++ 20
* [The Bazel build system](https://bazel.build/), or [GNU make](https://www.gnu.org/software/make/)
* [OpenSSL](https://www.openssl.org) version 1.1.0 or later, or optionally the [Intel IPP Cryptography Library](https://github.com/intel/ipp-crypto)

### scclib quick start

To test scclib:
* Install the [build essentials and OpenSSL development packages](https://github.com/stablecc/scclib/blob/master/dev_packages.md)
* Install [bazel](install_bazel.md)
* Download [scclib](https://github.com/stablecc/scclib)

Then run the following from the ```scclib``` directory:
```
$ bazel clean --expunge
$ ./all_tests_bazel.sh
```
This will test the current version of scclib and all support modules and repositories.
