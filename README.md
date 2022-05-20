# Test SSZ

Reproduces an issue where a list of Eth transactions panic when the hash_tree_root function is used.

# Steps

```
cargo test
```

```
running 1 test
test tests::test_ssz_list ... FAILED

failures:

---- tests::test_ssz_list stdout ----
thread 'tests::test_ssz_list' panicked at 'range end index 32 out of range for slice of length 0', /home/ubuntu/.cargo/git/checkouts/ssz_rs-bdb7e63807f0371b/8ce1efb/ssz_rs/src/list.rs:177:17
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace


failures:
    tests::test_ssz_list

test result: FAILED. 0 passed; 1 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
```