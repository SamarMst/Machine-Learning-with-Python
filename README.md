# Installation Guide

This guide covers the installation procedure for Windows 10 and later versions. It is based on the official [PyTorch installation procedure](https://pytorch.org/). If you have a GPU, the steps might get more complex, but this simplified procedure should work for most users.

> **Note:** Use the Command Prompt (cmd), not PowerShell.

## Course Instructor: MANEL SEKMA

## System Requirements
- A full installation (environment, data, notebooks) will require around **4GB** of disk space.

## Steps to Install

### 1. Install Python
A recent version of Python (3.9 to 3.10) is required. You can download Python from the official website:  
[https://www.python.org/downloads/](https://www.python.org/downloads/)

> **Note:** Version 3.11 and higher can sometimes cause compatibility issues.  
Ensure you select the option to **"Add Python to PATH"** during installation.

### 2. Create a Project Folder
It is recommended to keep all the files related to this project in one folder. You can create the folder using File Explorer or the Command Prompt.

For example, create a folder called `ML_python_tp`:
```bash
mkdir C:\ML_python_tp
```

### 3. Set Up a Python Virtual Environment
A virtual environment allows you to isolate the Python installation for this project, preventing it from affecting your system’s global Python installation.

Follow these steps to create and activate a virtual environment in the project folder:

1. Open the **Command Prompt (cmd)**.
2. Navigate to your project folder:
```bash
cd C:\ML_python_tp
```
3. Create a virtual environment in a subfolder named `ML_python_env`:
```bash
 python -m venv --system-site-packages ML_python_env
```
4. Activate the virtual environment:
```bash
 ML_python_env\Scripts\activate
```

> Once activated, the Command Prompt will enter virtual environment mode, meaning any Python or pip commands will apply to this environment rather than the system-wide installation.

### 4. Install Dependencies
Now, with the virtual environment active, you need to install the required packages:

1. Install the following essential libraries:
```bash
 pip3 install pandas numpy scipy scikit-learn Matplotlib seaborn
```
2. Install PyTorch according to your system requirements. For a CPU-based installation:
```bash
 pip3 install torch torchvision
```

> **Note:**  
`pip3` is the Python package manager.  
`torchvision` is a sub-module of PyTorch, specifically used for computer vision tasks.

### 5. View Installed Dependencies and Their Hierarchy
To manage and view dependencies in a structured way, you can use **Pipenv**, a package manager that helps manage dependencies and virtual environments.

1. Install Pipenv:
```bash
  pip3 install pipenv
```
2. View the dependency tree:
```bash
pipenv graph
```

### 6. Launch Jupyter Lab
To start working with notebooks, use **Jupyter Lab**. With your virtual environment activated, navigate to the project folder and run:
```bash
jupyter lab
```
