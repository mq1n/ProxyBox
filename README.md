# ProxyBox

This repository provides a ready to use Docker setup for running two popular proxy servers: **Squid** (HTTP/HTTPS proxy) and **Dante** (SOCKS5 proxy). Each proxy is containerized with its own configuration and can be easily deployed for development, testing, or production use.

## Getting Started

### Prerequisites
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)

### Build and Run
1. Clone this repository:
   ```sh
   git clone https://github.com/mq1n/ProxyBox
   cd ProxyBox
   ```
2. Build and start the services:
   ```sh
   docker compose up --build -d
   ```
3. Both proxies will be available on their respective ports (see below).

### Default Ports
- **Squid**: 3128
- **Dante**: 1080

## Configuration
- **Squid**: Edit `squid/squid.conf` and `squid/passwd` for custom rules and authentication.
- **Dante**: Edit `dante/danted.conf` for access control and settings.

## Stopping and Removing Containers
```sh
docker compose down
```

## License
MIT
