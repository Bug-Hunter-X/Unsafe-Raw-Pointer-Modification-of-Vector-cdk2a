# Unsafe Raw Pointer Modification of Vector in Rust

This repository demonstrates a common pitfall in Rust: attempting to modify a vector's contents through a raw pointer obtained using `as_mut_ptr()`.  This is unsafe and can lead to undefined behavior if not done carefully. The `bug.rs` file showcases the unsafe code, while `bugSolution.rs` presents a safer alternative using safe Rust mechanisms.  Always favor safe Rust methods over unsafe operations whenever possible.

## Bug Description:

The provided code snippet directly modifies the vector's data via a raw pointer.  This is problematic because it bypasses Rust's memory safety guarantees.  While it might appear to work in some cases, it's susceptible to crashes, data corruption, and other unpredictable behaviors due to issues like memory deallocation or out-of-bounds accesses.

## Solution:

The solution uses standard vector methods to avoid the use of raw pointers and maintain memory safety.