# Rusty Journal - Command-Line To-Do Tracker

Rusty Journal is a simple command-line to-do tracker written in Rust. It allows users to manage tasks by recording them in a JSON file, displaying them as a list in the terminal, and marking them as complete.

## Objectives

The main objectives of this project are:

- Develop a real-world command-line program using tested third-party crates for command-line parsing and error handling.
- Utilize third-party crates for enhanced functionality and better code organization.
- Implement features such as adding new tasks, removing completed tasks, and listing all tasks in the to-do list.
- Persist to-do items in a text file using a JSON format for data storage.

## Learning Topics

This project covers various learning topics, including:

- Setting up a Rust development environment.
- Creating, editing, and running Rust code using Cargo.
- Organizing code into multiple modules for better maintainability.
- Using third-party crates for improved functionality.
- Understanding common Rust concepts, including variables, data types, functions, and generic data types.

## Getting Started

### Prerequisites

Make sure you have Rust and Cargo installed on your system. If not, you can install them by following the instructions on the [official Rust website](https://www.rust-lang.org/learn/get-started).

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/eduardoraider/rust-cli-journal.git
   ```

2. Change into the project directory:

   ```bash
   cd rust-cli-journal
   ```

3. Build the application using Cargo:

   ```bash
   cargo build --release
   ```

## Usage

To interact with Rusty Journal, you can use the following command-line interface:

```bash
USAGE:
    rusty-journal [OPTIONS] <SUBCOMMAND>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
    -j, --journal-file <journal-file>    Use a different journal file

SUBCOMMANDS:
    add     Write tasks to the journal file
    done    Remove an entry from the journal file by position
    help    Prints this message or the help of the given subcommand(s)
    list    List all tasks in the journal file
```

## Example

```bash
$ cargo run -- -j test-journal.json add "buy milk"

$ cargo run -- -j test-journal.json add "take the dog for a walk"

$ cargo run -- -j test-journal.json add "water the plants"

$ cargo run -- -j test-journal.json list
1: buy milk                                           [2023-09-27 23:52]
2: water the plants                                   [2023-09-27 23:53]
3: take the dog for a walk                            [2023-09-28 00:24]

$ cargo run -- -j test-journal.json done 2

$ cargo run -- -j test-journal.json list
1: buy milk                                           [2023-09-27 23:52]
2: take the dog for a walk                            [2023-09-28 00:24]
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.

---

#### by Eduardo O Raider
🛠 🥋 **Software Engineer**