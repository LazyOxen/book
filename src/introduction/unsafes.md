Unsafes
=======

`unsafe` is a way to tell Rust that "I know what I'm doing!", which is necessary when writing extremely low-level code. You cannot write a kernel without `unsafe`s.

In that light, a kernel cannot be 100% safe, however the unsafe parts have to be marked with an `unsafe`, which makes the unsafe parts segregated from the safe code. We seek to eliminate the `unsafe`s where we can, and when we use `unsafe`s, we are extremely careful.

A quick grep gives us some stats: The kernel has 16.52% unsafe code, a 50% improvement in the last three weeks. Userspace has roughly ~0.2%.

In constrast to Linux, which has a code base with 100% unsafe code, due to the nature of C.

> TODO: Expand
