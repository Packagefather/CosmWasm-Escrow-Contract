# CosmWasm 101

Introduction to CosmWasm for 2023 Hackathon.

## Overview

In this repo you will find the content to match the CosmWasm 101 presentation for the Injective Global Hackathon 2023.

The introduction is split into 7 sections, numbered from 0-6, in order to navigate to a specific section checkout the git tags.

### Pre-Requisites

* Unix
* Terminal
* Git 2.37.1 or above

## Tutorial

### Section 0: Getting Started

First clone the repo:

```bash
$ git clone https://github.com/InjectiveLabs/cosmwasm101.git
$ cd cosmwasm101
$ git checkout section-0
```

Here you find an empty repo, with nothing but this `README.md` to see. If you got this far you probably have got the relevant pre-requisites installed.

Navigate to sections 1 in order to find the instructions to get the environment setup:

```bash
$ git checkout section-1
```

### Section 1: Environment Setup

Now setup the development environment. You will need to install:

* [Rust](https://www.rust-lang.org/tools/install)
* CosmWasm
* [Cargo Generate](https://github.com/cargo-generate/cargo-generate)

First download rust:

```bash 
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
$ rustup default stable
```

Check rust has successfully been installed:

```bash
$ cargo version
$ cargo 1.67.1 (8ecd4f20a 2023-01-10)
```

**Note:** If version is lower than 1.55 we need to update run command `$ rustup update stable`

Next add the CosmWasm targets:

```bash
$ rustup target add wasm32-unknown-unknown
```

Finally install `cargo generate` this will help us quickly launch a new CosmWasm project.

```bash
$ cargo install cargo-generate --features vendored-openssl
$ cargo install cargo-run-script
```

#### Recommendec IDE Plugins

You may wish you install helpful plugins for your IDE:

* [VS Code: Rust Analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)
* [Jet Brains](https://www.jetbrains.com/rust/)
