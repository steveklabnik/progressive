progressive
===========

A rust library for showing progress of iterators and loops.

### Documentation

To create the documentation run:

```
cargo doc
```

### Usage

To use `progressive`, add this to your `Cargo.toml`:

```toml
[dependencies]
progressive = "0.1"
```

And this to your crate root:

```rust
extern crate progressive;
```

Here's a simple example that shows how to wrap an iterator tin order to get progress information:

```rust
extern crate progressive;

use progressive::progress;
use std::time::Duration;

fn main() {
    for _ in progress(0..30) {
        // do something expensive here
        std::thread::sleep(Duration::from_millis(200));
    }
}
```

For an example run `cargo run --example basic`
