# cbr-issue-284-demo
Demo of cargo-bisect-rustc issue 284

See discussion in https://github.com/rust-lang/cargo-bisect-rustc/issues/284

You can observe the problem(s) yourself by attempting a bisect via:

```
cargo bisect-rustc --preserve --start 1.63.0 --end 1.71.0 --access github
```

In principle, given the `.cargo/config.toml` that is in place, that should flag the regression as taking place in nightly-2022-08-02. However, during my current uses of cargo-bisect-rustc, it seems like the tool is repeatedly flagging the regression as still occuring in nightly-2023-03-12 (which is the nightly that gets flagged if you aren't using any `.cargo/config.toml` at all...)
