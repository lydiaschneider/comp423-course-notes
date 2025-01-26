### My Guide to Rust

* Primary author: [Lydia Schneider](https://github.com/lydiaschneider)
* Reviewer: [Akshaya Sundar](https://github.com/sundarak)

Hello and welcome to my beginner's guide to Rust:


Here are some prerequisites before we get started:
1) A GitHub account
2) Git installed
3) VS Code downloaded
4) Docker installed
5) Knowledge of command-line basics


Ok let's get started with Rust!!

Part 1: Project Setup: Creating a Repository
1.1) Open your terminal and create a new directory for you project with the following commands

mkdir rust-dev-container
cd rust-dev-container

1.2) Initialize a Git repository with the following command

git init

1.3) Create a README file:

echo "# Rust DevContainer Setup" > README.md
git add README.md
git commit -m "Initial commit with README"


1.4) Log into GitHub and navigate to the Create a New Repository page
1.5) Fill out the following details
        Repository name: rust-devcontainer
        Description: "Rust project setup using Dev Containers"
        Visibility: Public
1.6) Click Create Repository
1.7) Link your local repository to GitHub with the following commands:

git remote add origin https://github.com/<your-username>/rust-devcontainer.git
git branch -M main
git push --set-upstream origin main

Part 2: Setting Up the Dev Container
2.1) Make sure Docker is running and create a .devcontainer directory and configuration file with the following code:


mkdir .devcontainer
cd .devcontainer
echo '{
  "name": "Rust DevContainer",
  "image": "mcr.microsoft.com/devcontainers/rust:latest",
  "extensions": ["rust-lang.rust-analyzer"]
}' > devcontainer.json

2.2) Open the project in VS Code

code ..

2.3) When prompted, Reoped in Container to start to Dev Container
2.4) Once inside the container, verify Rust is installed:

rustc --version

Part 3: Writing and Running Your First Rust Program
3.1) Create a new Rust project with the following commands

cargo new hello_comp423 --vcs none
cd hello_comp423

3.2) To write the "Hello COMP423", edit src/main.rs and replace the contents with the following:

fn main() {
    println!("Hello COMP423");
}

3.3) Build the project:

cargo build

3.4) Compile and run the project: 

cargo run

This command compiles and runs the project in a single step whereas cargo build only compiles the code without executing it. This is similar to how gcc compiles programs in C, except you must run the executable manually.

3.5) Pushing final changes to GitHub

git add .
git commit -m "Your message here"
git push

3.6) Ensure changes were made to you GitHub repository

Congratulations! You've successfully set up a Rust Dev Container, written a program & pushed it to GitHub!


 
