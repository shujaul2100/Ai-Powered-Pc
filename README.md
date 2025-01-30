# Ai-Powered-Pc

Front End:

![image](https://github.com/user-attachments/assets/c5ee70ca-397a-4c6e-b5fc-12b0f4ce9393)

Back End Server:

![image](https://github.com/user-attachments/assets/27a95a2c-2aae-4ed4-aca7-0714b24db0de)


## my current Configuration:

![image](https://github.com/user-attachments/assets/34d66031-c1e7-4cb6-9f19-c01415e40ca7)

Clone this repository

``
 git clone https://github.com/shujaul2100/AI_POWERED_PC.git

``

Paal Ai Frontend has build as well as the code both which can be used to run the frontend

Paal Ai Backedn has the backend server code.

Note: First run the backend server then run frontend ui , or else you will network error on the ui if backend server is not running.

# Pre-Requiste:


---

## Specific Version Installation Guide for Python, Node.js, npm, and Rust

## Python (Version 3.12.0)
### Windows:
1. Download the specific Python version installer from the [Python Releases for Windows page](https://www.python.org/downloads/windows/).
2. Select Python 3.12.0, download the executable installer, and run it. Ensure that you check "Add Python to PATH" before clicking "Install Now."

### macOS:
1. Use `pyenv` to manage multiple Python versions:
   ```bash
   brew install pyenv
   pyenv install 3.12.0
   pyenv global 3.12.0
   ```

### Linux (Ubuntu):
1. Use `pyenv` to install and manage Python versions:
   ```bash
   sudo apt-get update
   sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
   libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
   xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
   curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
   pyenv install 3.12.0
   pyenv global 3.12.0
   ```

## Node.js (Version 18.20.6) and npm (Version 10.8.2)
### All Platforms:
1. The best way to install specific versions of Node.js and npm is via `nvm` (Node Version Manager).
   - **Windows:** Use [nvm-windows](https://github.com/coreybutler/nvm-windows/releases)
   - **macOS/Linux:** Use [nvm](https://github.com/nvm-sh/nvm)
2. Install nvm and then run:
   ```bash
   nvm install 18.20.6
   nvm use 18.20.6
   npm install -g npm@10.8.2
   ```

## Rust (Version 1.84.0)
### All Platforms:
Rustup manages Rust versions:
1. Install `rustup` if not already installed:
   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```
2. Install the specific version of Rust:
   ```bash
   rustup install 1.84.0
   rustup default 1.84.0
   ```

## Warning for Open Interference Library
**Warning:** The Open Interference library requires Python version 3.12.0 or later. Using earlier versions of Python may lead to compatibility issues or unexpected behavior. Always verify that the correct version of Python is activated in your environment before running scripts that depend on the Open Interference library.

### Verify Installation
After installation, verify that the correct versions are installed:
```bash
python --version   # Should output Python 3.12.0
node -v            # Should output v18.20.6
npm -v             # Should output 10.8.2
rustc --version    # Should output rustc 1.84.0
```


Here’s a document designed to guide you through setting up and configuring the frontend of your application, specifically for a project structured under `paal-ai-frontend`. The document outlines two methods for getting your application up and running.

---

# Frontend Configuration and Setup Guide

This document details the processes for setting up the frontend of your application. There are two primary methods to prepare and launch the frontend from the `paal-ai-frontend` directory in your cloned repository.

## Prerequisites
Ensure that you have Node.js and npm installed on your system to handle dependencies and run the project. Verify installation by running `node -v` and `npm -v` in your command line.

## Method 1: Using Pre-built Files

### Step 1: Locate the Build Directory
In your cloned repository, navigate to the `paal-ai-frontend\build` directory. This directory contains a pre-built version of your frontend, compiled and ready to be served.

### Step 2: Serve the Build Directory
To serve the static files in the `build` directory, you can use a static server. If you don’t have a static server installed, you can use `serve`, a simple static server provided by npm.

1. Install `serve` globally (if not already installed):
   ```bash
   npm install -g serve
   ```
2. Serve your application:
   ```bash
   serve -s paal-ai-frontend/build
   ```

This will start a local server to host your frontend. The terminal will display the URL at which the app is being served, typically `http://localhost:5000`.

![image](https://github.com/user-attachments/assets/f61e7a44-5d9d-4d0f-8229-e2edc5d9725b)


## Method 2: Using Source Code

### Step 1: Navigate to the Frontend Directory
Change into the `paal-ai-frontend` directory in your cloned repository:
```bash
cd path/to/cloned/repository/paal-ai-frontend
```

### Step 2: Install Dependencies
Ensure all dependencies are correctly installed. If you encounter issues with the packages or `node_modules`:

1. Remove the existing `node_modules` directory:
   ```bash
   rm -rf node_modules
   ```
2. Reinstall all dependencies:
   ```bash
   npm install
   ```

### Step 3: Start the Application
Once dependencies are installed, start the frontend application:
```bash
npm start
```

This command will compile the source code and typically launch your browser to `http://localhost:3000`, where the app will be running. It also watches for any changes in the source files and automatically reloads the browser.

![image](https://github.com/user-attachments/assets/4f8174c1-8cf2-4a6b-ad28-bd2515c56009)


## Troubleshooting

- **Dependency Issues**: If you see errors related to missing modules or dependencies, ensure that `npm install` completes without errors.
- **Port Conflicts**: If `npm start` indicates that the port is already in use, you can specify a different port by modifying the scripts in your `package.json` or running `PORT=XXXX npm start`, where `XXXX` is your desired port number.

## Conclusion

This guide provides two methods for setting up and running the frontend of your application. Method 1 is straightforward and best for quick previews or production environments where changes are not anticipated. Method 2 is suited for development and testing, allowing real-time updates as changes are made to the code.

---

Ensure to distribute this guide among your development team and anyone involved in deploying or testing the frontend of your application. This will help maintain consistency and efficiency in your development workflow.

# Backend Configuration and Running Guide

This document provides a comprehensive guide to setting up and running the backend of your application using Rust, the Open Interference library,configuring the OpenAI API key in the `server-backend.py` file ,FastAPI, and Uvicorn.

## Prerequisites
Ensure that Python and Rust are installed on your system as they are required for running the backend and associated libraries.

## Step 1: Verify Rust Installation

Confirm that Rust is installed by executing:

```bash
rustc --version
```

If Rust is not installed, follow the installation instructions on the [official Rust installation page](https://www.rust-lang.org/tools/install).

## Step 2: Install the Open-Interference Library

Install the library using pip:

```bash
pip install open-interpreter
```

For detailed installation guidelines, visit the [Open Interpreter Setup Documentation](https://docs.openinterpreter.com/getting-started/setup).

## Step 3: Install FastAPI and Uvicorn

FastAPI is utilized for building APIs, and Uvicorn serves as the ASGI server:

```bash
pip install fastapi uvicorn
```

## Step 4: Configure Your OpenAI API Key

Before running your server, ensure to configure your OpenAI API key in the `server-backend.py` script. Replace the empty string for `api_key` with your actual API key.

```python
interpreter.llm.api_key = "your_openai_api_key_here"
```

For more information on obtaining and using your API key, please refer to the [OpenAI API documentation](https://docs.openinterpreter.com/language-models/hosted-models/openai).

## Step 5: Start the Backend Application

Navigate to the directory containing your FastAPI application code. Assuming your backend code is in `paal-ai-backend`:

```bash
cd path/to/cloned/repository/paal-ai-backend
```

Run the server with Uvicorn:

```bash
uvicorn server-backend:app --reload
```

This starts the server on `localhost` with default port `8000` and enables hot reload.

This is how after successful backend server launch will look like:

![image](https://github.com/user-attachments/assets/62fbc7b3-b4df-4326-b31d-8a3f26c6ad4d)

## Accessing Your API

Access your API via:

```
http://localhost:8000
```

Use this URL in a web browser or API testing tools like Postman to interact with your API endpoints.




