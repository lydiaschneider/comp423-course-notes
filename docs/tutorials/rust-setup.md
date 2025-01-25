* Primary author: [Lydia Schneider](https://github.com/lydiaschneider)

Welcome to your Rust tutorial!

Before we get started, here are some things you need:
- Have VSCode downloaded on your computer. If you don't, follow this link: https://code.visualstudio.com/)
- Basic knowledge of Git and Docker

Step 1: Initialize a New Git Repository

1.1) mkdir rust-dev-container 
1.2) cd rust-dev-container
1.3) git init

Step 2: Create a DevContainter Configuration
2.1) Create a .devcontainer directory and a devcontainer.json file inside it
2.2) Edit the configuration of the json file so it looks something like this:

{
    "name": "Rust Dev Container",
    "image": "mcr.microsoft.com/vscode/devcontainers/rust:latest",
    "features": {
        "rust-analyzer": "latest"
    }
}

Step 3: Create a Rust Project
3.1) Create the new project without initializing a new repo: cargo new hello-comp423 --vcs none
3.2) Cd into that new project: cd hello-comp423

Step 4: Write a Basic Program
4.1) Open src/main.rs
4.2) Add the following Rust code:

fn main() {
    println!("Hello COMP423");
}

Step 5: Build and Run the Program
5.1) Compile the program: cargo build
5.2) Run the program: cargo run

 
