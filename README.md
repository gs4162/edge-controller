Here’s a basic README for your **edge-controller** repository:

---

# Edge Controller

This repository contains the starting stack for deploying an edge controller system. The stack includes **Ignition**, **Ignition Edge**, a **MySQL database**, and tools for hardware testing.

## Components

- **Ignition**: Industrial automation platform for SCADA, HMI, and IIoT systems.
- **Ignition Edge**: Lightweight version of Ignition designed for edge-of-network devices.
- **MySQL**: Database used for storing project data.
- **Testing Tools**: Scripts and configurations for hardware testing.

## How to Use

1. Clone this repository:
    ```bash
    git clone https://github.com/gs4162/edge-controller.git
    ```

2. Navigate to the directory and start the stack using Docker Compose:
    ```bash
    cd edge-controller
    docker-compose up
    ```

3. Access Ignition or Ignition Edge by visiting their respective web interfaces after the containers are up.

## Directory Structure

- `/ansible`: Automation playbooks for configuring the system.
- `/ignition-edge`: Contains the configuration for Ignition Edge.
- `/ignition-standard`: Contains the configuration for the full Ignition platform.
- `/mysql`: Database configuration files.
- `/testing`: Scripts and tools for hardware testing.

## Contributing

Feel free to submit issues or pull requests to improve the project.

---

This README gives an overview of the project and basic usage instructions.
