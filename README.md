Cargo downloads your Rust project’s dependencies and compiles your project.

Learn more at http://crates.io/.

## Installing cargo from nightlies

Cargo has nightlies available for use. The cargo source is not always guaranteed
to compile on rust master as it may lag behind by a day or two. Nightlies,
however, will run regardless of this fact!

```sh
triple=x86_64-unknown-linux-gnu
curl -O http://static.rust-lang.org/cargo-dist/cargo-nightly-$triple.tar.gz
tar xf cargo-nightly-$triple.tar.gz
./cargo-nightly-$triple/install.sh
```

Nightlies are available for the following triples:

* [`x86_64-unknown-linux-gnu`](http://static.rust-lang.org/cargo-dist/cargo-nightly-x86_64-unknown-linux-gnu.tar.gz)
* [`i686-unknown-linux-gnu`](http://static.rust-lang.org/cargo-dist/cargo-nightly-i686-unknown-linux-gnu.tar.gz)
* [`x86_64-apple-darwin`](http://static.rust-lang.org/cargo-dist/cargo-nightly-x86_64-apple-darwin.tar.gz)
* [`i686-apple-darwin`](http://static.rust-lang.org/cargo-dist/cargo-nightly-i686-apple-darwin.tar.gz)
* [`i686-pc-mingw32`](http://static.rust-lang.org/cargo-dist/cargo-nightly-i686-pc-mingw32.tar.gz)

Note that if you're using the windows snapshot you will need Mingw-w64 installed
as well as MSYS. The installation script needs to be run inside the MSYS shell.

## Compiling cargo

Cargo requires the following tools and packages to build:

* `rustc`
* `python`
* `curl` or `wget`
* `cmake`
* `pkg-config`
* OpenSSL headers (`libssl-dev` package on ubuntu)

Cargo can then be compiled like many other standard unix-like projects:

```sh
git clone https://github.com/rust-lang/cargo
cd cargo
./configure
make
make install
```

More options can be discovered through `./configure`, such as compiling cargo
for more than one target. For example, if you'd like to compile both 32 and 64
bit versions of cargo on unix you would use:

```
$ ./configure --target=i686-unknown-linux-gnu,x86_64-unknown-linux-gnu
```

## Contributing to the Docs

To contribute to the docs, please submit pull requests to [wycats/cargo-website][1].
All you need to do is change the markdown files in the source directory.

[1]: https://github.com/wycats/cargo-website

## Reporting Issues

Found a bug? We'd love to know about it!

Please report all issues on the github [issue tracker][issues].

[issues]: https://github.com/rust-lang/cargo/issues

## License

Cargo is primarily distributed under the terms of both the MIT license
and the Apache License (Version 2.0).

See LICENSE-APACHE and LICENSE-MIT for details.
