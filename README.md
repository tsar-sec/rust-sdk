# TSAR Client API

The official Rust SDK for TSAR. Rust is our primary focus, so this SDK will be the most maintained.

## Example Import

```toml
tsar-client = "*"
```

## Example Usage

```rs
use tsar_client::Client;

// Get these credentials from: https://tsar.cc/app/any/settings
const CLIENT_KEY: &str = "MFkwEwY...GAr/ITBqA==";
const APP_ID: &str = "00000000-0000-0000-0000-000000000000";

fn main() {
    let client = Client::new(APP_ID, CLIENT_KEY).expect("Failed to initialize client");

    // If client formed successfully, then the user is authorized
    // Access user info directly from the client

    println!("Username: ", client.subscription.user.username);
}
```
