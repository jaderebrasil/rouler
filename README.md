# roller

A container-like system for generating dice rolls

## Usage

roller is a Rust library for generating die rolls from convenient little state containers. A die roll can be created and stored and called repeatedly to generate new values.

This allows easy use and re-use of specific die rolls, and even comparison. 

```rust
extern crate roller;

use roller::Roller;

let mut let mut stat = Roller::new("3d6");

println!("STR: {}", stat.total());
println!("DEX: {}", stat.reroll());

println!("Last stat roll: {}", stat);

let att = Roller::new("1d20 + 5");
let def = Roller::new("1d20 + 2");

if att > def {
    println!("You struck the monster!");        
} else {
    println!("You missed!");
}
```

## License

This Source Code Form is subject to the terms of the Mozilla Public
License, v. 2.0. If a copy of the MPL was not distributed with this
file, You can obtain one at http://mozilla.org/MPL/2.0/.