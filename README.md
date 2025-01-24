# playground-duckdb

A repository that uses Daytona to create a DuckDB playground for users like data analysts and scientists to interact

## Introduction

This repository provides a streamlined solution to deploy and run DuckDB in a Daytona Dev Environment. It simplifies the process of setting up a ready-to-use environment for data analysts and scientists to interact with DuckDB.

### Purpose

The primary purpose of this project is to provide a reliable, high-performance environment to run and interact with DuckDB efficiently. It aims to address the challenges faced by data analysts and scientists in setting up and maintaining a DuckDB environment.

### Key Benefits:
- **Ease of use**: Simplifies the setup and deployment process.
- **Scalability**: Facilitates working with large datasets and complex queries without the need to configure hardware or software.

## Setup

### Prerequisites

To use this Devcontainer, you'll need:
- **An IDE:** Such as Visual Studio Code (VS Code) or JetBrains, with the latest version installed.
- **Daytona:** An open-source development management platform. More info [here](https://www.daytona.io/).
- **Docker:** A container technology. Download link [here](https://docs.docker.com/get-started/get-docker/).

### Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/c0d33ngr/playground-duckdb.git
   ```

2. **Set up the workspace for DuckDB playground using Daytona:**
   ```bash
   daytona create https://github.com/c0d33ngr/playground-duckdb.git
   ```

3. **Open the workspace in your preferred IDE:**
   ```bash
   daytona code playground-duckdb
   ```

### Dev Container Configuration

The `devcontainer.json` file in this repository defines the specific environment configuration. It includes details such as:

```json
{
    "name": "DuckDB Playground",
    "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
    "features": {
        "ghcr.io/eitsupi/devcontainer-features/duckdb-cli:1": {},
        "ghcr.io/devcontainers/features/python:1": {}
    },
    "postCreateCommand": "pip install duckdb matplotlib pandas"
}
```

### Customization

You can customize the configuration to suit your specific needs. Refer to the official Devcontainers documentation for more details on available options: [here](https://containers.dev/implementors).

## Usage

### Prerequisites

Ensure you have the necessary prerequisites installed as mentioned in the Setup section.

### Installation

Follow the setup instructions to get your DuckDB environment up and running.

## Contribution

Contributions to the repository are welcome. Feel free to open an issue or submit a PR for any changes, bugs, or features you think are worth adding.

## Notes/Issues

If you encounter any problems or have questions, don't hesitate to open an issue.

Feel free to refine and expand this template with any additional information specific to your repository.
