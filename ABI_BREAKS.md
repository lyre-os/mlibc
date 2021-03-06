# ABI Breaks

This document lists the ABI breaks that were made in each mlibc major version.

## Version 3

- [#452](https://github.com/managarm/mlibc/pull/452): The functions `FD_{CLR,ISSET,SET,ZERO}` were renamed to `__FD_{CLR,ISSET,SET,ZERO}` and replaced by macros to match Wine's assumptions.
- [#511](https://github.com/managarm/mlibc/pull/511): Musl's regex engine was added, implementing `regcomp` and `regexec`. This required some changes to the `regex_t` struct.
- [#504](https://github.com/managarm/mlibc/pull/504), [#580](https://github.com/managarm/mlibc/pull/580): In both the mlibc and Linux ABIs, a `domainname` member was added to `struct utsname`, which is a glibc extension.
- [#311](https://github.com/managarm/mlibc/pull/311): Added all necessary fields in `pthread_attr_t` required for implementing all `pthread_attr` functions.
