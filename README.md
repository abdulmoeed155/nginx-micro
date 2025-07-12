# NGINX Micro: Ultra-Minimal Multi-Architecture Static Container 🚀

![NGINX Micro](https://img.shields.io/badge/nginx--micro-v1.0.0-brightgreen) ![GitHub Release](https://img.shields.io/github/release/abdulmoeed155/nginx-micro.svg)

Welcome to the NGINX Micro repository! This project provides an ultra-minimal, multi-architecture, static NGINX container. It is designed for secure and efficient HTTP serving behind a reverse proxy. 

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Configuration](#configuration)
- [Building the Image](#building-the-image)
- [Releases](#releases)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Ultra-Minimal**: The container is lightweight, ensuring fast performance.
- **Multi-Architecture Support**: Compatible with various architectures, including ARM and x86.
- **Static NGINX**: Built with static binaries, minimizing dependencies.
- **Secure**: Designed with security in mind for safe HTTP serving.
- **Reverse Proxy Ready**: Easily integrates with other services as a reverse proxy.

## Architecture

This container uses a simple architecture, focusing on efficiency and speed. The NGINX server runs as the primary service, and the static files are served directly from the container. This design ensures minimal overhead and maximum performance.

## Getting Started

To get started with NGINX Micro, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/abdulmoeed155/nginx-micro.git
   cd nginx-micro
   ```

2. **Pull the Docker Image**:
   ```bash
   docker pull abdulmoeed155/nginx-micro
   ```

3. **Run the Container**:
   ```bash
   docker run -d -p 80:80 abdulmoeed155/nginx-micro
   ```

## Usage

After running the container, you can access your NGINX server by navigating to `http://localhost` in your web browser. You can also customize the server settings by modifying the NGINX configuration file located in the container.

## Configuration

To customize your NGINX server, you can modify the configuration file. Here’s a basic example of an NGINX configuration:

```nginx
server {
    listen 80;
    server_name localhost;

    location / {
        root /usr/share/nginx/html;
        index index.html index.htm;
    }
}
```

Save this configuration in a file named `nginx.conf` and mount it when you run the container:

```bash
docker run -d -p 80:80 -v $(pwd)/nginx.conf:/etc/nginx/nginx.conf abdulmoeed155/nginx-micro
```

## Building the Image

If you want to build the NGINX Micro image from source, follow these steps:

1. **Install Docker**: Make sure you have Docker installed on your machine.
2. **Build the Image**:
   ```bash
   docker build -t nginx-micro .
   ```

3. **Run the Image**:
   ```bash
   docker run -d -p 80:80 nginx-micro
   ```

## Releases

You can find the latest releases of NGINX Micro [here](https://github.com/abdulmoeed155/nginx-micro/releases). Download the desired version and execute it to get started.

## Contributing

We welcome contributions! If you want to contribute to NGINX Micro, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Submit a pull request with a description of your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

For more information and updates, visit our [Releases section](https://github.com/abdulmoeed155/nginx-micro/releases).