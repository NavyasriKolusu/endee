# Endee: High-Performance Open Source Vector Database

Endee (nD) is a high-performance, open-source vector database designed for fast and efficient vector similarity search. As part of this project, I explored Endee by building and running it locally using multiple supported approaches to understand its build system, runtime behavior, and deployment options.

This document summarizes the system requirements, installation methods, and execution steps that I personally followed while working with Endee.


## Ways to Build and Run Endee

During this project, I worked with the following supported methods to build and run Endee:

1. Quick installation and execution using the provided `install.sh` and `run.sh` scripts  
2. Manual build using CMake for deeper control  
3. Docker-based deployment  

Endee can also be run directly using a pre-built Docker image from Docker Hub without building it locally (described in Section 4).


## System Requirements

Before building or running Endee, ensure your system meets the following requirements.

### Supported Operating Systems

- **Linux**:  
  Ubuntu (22.04, 24.04, 25.04)  
  Debian (12, 13)  
  Rocky Linux (8, 9, 10)  
  CentOS (8, 9, 10)  
  Fedora (40, 42, 43)

- **macOS**:  
  Apple Silicon (M-series) only

### Required Dependencies

The following dependencies are required to compile Endee from source:

- clang-19  
- cmake  
- build-essential  
- libssl-dev  
- libcurl4-openssl-dev  

> **Note:** Endee requires Clang 19 (or a compatible recent version) with C++20 support.

## 1. Quick Installation 

The simplest way to build Endee is by using the provided `install.sh` script.  
This script automatically detects the operating system, verifies dependencies, and configures the build.

### Usage

Make the script executable:

```bash
chmod +x ./install.sh
