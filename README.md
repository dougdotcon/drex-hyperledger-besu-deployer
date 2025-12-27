# DrexBesuDeployer

![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)
![Docker](https://img.shields.io/badge/Docker-Ready-blue?logo=docker)

## Overview

**DrexBesuDeployer** is a robust orchestration tool designed to streamline the setup and deployment of Hyperledger Besu nodes. Inspired by the architectural principles of **Drex** (Brazil's Central Bank Digital Currency), this tool allows developers and enterprises to bootstrap a production-grade QBFT or IBFT network in seconds, eliminating complex manual configurations.

[![Docker & Docker Compose Tutorial](https://i.ibb.co/7bc5K4v/CBDC3-MINUTES.jpg)](https://www.youtube.com/watch?v=wcjsAaBnzNI)

## Key Features

*   **Rapid Deployment:** Initialize a multi-node Besu network with a single command.
*   **Automated Key Management:** Automatically generates cryptographic keys for every node in the consensus layer.
*   **Containerized Architecture:** Leverages Docker and Docker Compose for isolated, consistent environments.
*   **User-Friendly Interface:** Interactive CLI for specifying node counts and network topology.

## Prerequisites

Before proceeding, ensure the following are installed and running on your system:

*   **Docker Engine:** Version 20.10+
*   **Docker Compose:** Version 1.29+
*   **Bash Shell:** (Linux/macOS native, Windows users require Git Bash or WSL)

## Installation & Setup

### 1. Install Docker

**Windows / macOS:**
Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop). It includes Docker Compose by default.

**Linux (Ubuntu/Debian):**
bash
# Update package index
sudo apt-get update

# Install Docker Engine
sudo apt-get install docker-ce docker-ce-cli containerd.io

# Install Docker Compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose


### 2. Deploy the Network

1.  Clone the repository:
    bash
    git clone https://github.com/your-username/drex-besu-deployer.git
    cd drex-besu-deployer
    

2.  Run the installation script:
    bash
    sh install.sh
    
    *Note: This script verifies your Docker environment and initializes the necessary configurations.*

## Usage

After installation, follow the on-screen prompts to specify the number of nodes and network parameters. The tool will generate a `docker-compose.yml` file and start the containers automatically.

## Project Structure

*   `Dockerfile`: Defines the custom Besu node image.
*   `qbftConfigFile.json`: Consensus configuration template.
*   `install.sh`: Bootstrap script to validate dependencies and prepare the environment.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This tool is an open-source utility for educational and development purposes. It is not affiliated with or endorsed by the Central Bank of Brazil or any official Drex project entities.