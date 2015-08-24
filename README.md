# episode-002
Where we use cargo to setup a Rust project

## Setup
The following needs to be prepared

* Terminal with access to `cargo`

## Script

We can use `rustc` to compile [Rust][rust-lang] programs, but even for small projects this gets unwieldly. When we installed [Rust][rust-lang] another tool became available: `cargo`.

`cargo` is a jack of all trades for [Rust][rust-lang], but in this episode we focus on building a [Rust][rust-lang] project.

By executing the command

```sh
cargo new hello --bin
```

a directory `hello` is created with the following structure

```
hello
├── Cargo.toml
└── src
    └── main.rs
```

With a quick glance into `main.rs` we discover the familiar "Hello, World!" program. When we enter the just created directory `hello` and execute

```sh
cargo build
```

the project is build in `debug`-mode. We will talk about `Cargo.toml` and `Cargo.lock` in an other episode. For now we look into the `target` directory.

```
target
└── debug
    ├── build
    ├── deps
    ├── examples
    ├── hello
    ├── hello.dSYM
    │   └── Contents
    │       ├── Info.plist
    │       └── Resources
    │           └── DWARF
    │               └── hello
    └── native
```

For now the most important part is the `target/debug/hello` executable. We could run it by calling it directly, but instead the `cargo` command can be used as well.

By issuing

```sh
cargo run
```

`target/debug/hello` is executed.

And there you have it, we used `cargo` to create and build a [Rust][rust-lang] project.


[rust-lang]: https://www.rust-lang.org/