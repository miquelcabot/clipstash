# ClipStash

ClipStash is a web application that allows users to save and organize text clips. Users can create, read, update, and delete clips. Clips are stored in a SQLite database.

## Running the project

To run the project, you will need to have Rust installed. You can install Rust by following the instructions at [https://www.rust-lang.org/tools/install](https://www.rust-lang.org/tools/install).

After installing Rust, you can clone the repository and navigate to the project directory. You can then run the following command to start the project:

```
cargo run --bin name
```

where `name` is the name of the binary you wish to run.

To check the project for errors, you can run the following command:

```
cargo check
```

To run the tests for the project, you can run the following command:

```
cargo test
```

## Rocket configuration issues

If you are getting compilation errors related to `rocket::response::content::Html` or `rocket::response::content::RawHtml` then run these commands to fix:

```
cargo update --package rocket --precise 0.5.0-rc.1
cargo update --package rocket_codegen --precise 0.5.0-rc.1
cargo update --package rocket_http --precise 0.5.0-rc.1
```

## SQLx configuration
The ClipStash project requires additional steps in order to properly build. You will need the `sqlx-cli` tool which can be installed by running

```
cargo install sqlx-cli
```

After installing the tool, you can configure the database for the project by running

```
sqlx database setup