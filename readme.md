# Key Takeaways

- [01. Guessing Game](#01-guessing-game)

## 01. Guessing Game

<details>
  <summary>Using External Crates (Packages)</summary>
  <p>In Rust, external crates (packages) can be imported using the `Cargo.toml` file. These crates provide additional functionality not found in the standard library.</p>
</details>

<details>
  <summary>Immutable Variables by Default</summary>
  <p>Rust enforces immutability by default. However, you can make variables mutable by using the `mut` keyword. Example:</p>
  <pre><code>let mut guess = String::new();</code></pre>
</details>

<details>
  <summary>The `::` Operator</summary>
  <p>The `::` operator is used in Rust to access functions or types that are associated with a module, struct, or enum. Example:</p>
  <pre><code>use std::io;</code></pre>
</details>

<details>
  <summary>Pattern Matching with `match`</summary>
  <p>Rust’s `match` expression allows for control flow based on pattern matching. In this example, `match` is used to compare the user’s guess to the secret number using `cmp` from the `std::cmp::Ordering` enum:</p>
  
```rust
match guess.cmp(&secret_number) {
    Ordering::Less => println!("Too small!"),
    Ordering::Greater => println!("Too big!"),
    Ordering::Equal => {
        println!("You win!");
        break;
    }
}
```
</details>

<details>
  <summary>Enums in Rust</summary>
  <p>In Rust, enums are a powerful feature that allows you to define a type that can be one of several variants. This is evident in the `Ordering` enum used with `cmp`, which can be `Less`, `Greater`, or `Equal`. Additionally, `Result` is an enum that encapsulates success (`Ok`) or failure (`Err`). This makes it easier to write robust error handling and control flow through pattern matching. For example:</p>

```rust
match guess.cmp(&secret_number) {
    Ordering::Less => println!("Too small!"),
    Ordering::Greater => println!("Too big!"),
    Ordering::Equal => {
        println!("You win!");
        break;
    }
}
```

</details>
