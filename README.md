# LEVIKO TUNNEL

**LEVIKO TUNNEL** is a branded, high-performance reverse tunneling project for controlled TCP/UDP forwarding, multiplexed connections, WebSocket transports, and real-time node monitoring.

> This distribution is presented as **LEVIKO TUNNEL**. The implementation retains the licensing obligations of the upstream work from which it was derived.

## What is different in this distribution?

- A dedicated **LEVIKO TUNNEL** identity throughout the application.
- A redesigned server dashboard with its own visual language and navigation.
- Branded startup/runtime output instead of generic project naming.
- Dedicated telemetry labels for LEVIKO traffic, ports, connections, and system resources.
- Repository/release references configured for `danesh1118/LEVIKOTUNNEL`.
- Default sniffer log name: `leviko-tunnel.json`.

## Quick start

### Build

```bash
git clone https://github.com/danesh1118/LEVIKOTUNNEL.git
cd LEVIKOTUNNEL
go build -o leviko-tunnel .
```

### Run

```bash
./leviko-tunnel -c /path/to/config.toml
```

The program supports separate **server** and **client** configurations. The configuration format is TOML.

## Server dashboard

When the web monitoring interface is enabled by the server configuration, open the configured web port in a browser.

The interface is intentionally branded as **LEVIKO TUNNEL** and provides:

- Tunnel status
- CPU, RAM, disk and swap telemetry
- Network and LEVIKO traffic counters
- Upload/download rates
- Active connection information
- Port usage telemetry
- Sniffer status
- Light/dark presentation

## Supported transport capabilities

Depending on configuration, LEVIKO TUNNEL supports:

- TCP
- UDP
- WebSocket (WS)
- Secure WebSocket (WSS)
- TCP multiplexing
- WebSocket multiplexing
- UDP forwarding over supported transports
- TLS-backed transports
- Keepalive and heartbeat controls
- Hot configuration reload
- Optional traffic usage monitoring

## Configuration

Use the existing TOML configuration structure supplied with the project.

A minimal server invocation is:

```bash
./leviko-tunnel -c server.toml
```

A client invocation uses the same binary with a client configuration:

```bash
./leviko-tunnel -c client.toml
```

Do not expose management or monitoring ports to the public internet unless you have intentionally secured them with your own network controls.

## Repository

Official repository target:

`https://github.com/danesh1118/LEVIKOTUNNEL`

## Branding

**LEVIKO TUNNEL** is the product identity used by this distribution. The project UI, runtime messages, README, release metadata, and default monitoring terminology are intentionally branded around LEVIKO.

## License

See [`LICENSE`](LICENSE).

This project is based on software distributed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. The license terms and attribution requirements remain applicable to the covered source code.

## Notice

This README documents the LEVIKO TUNNEL distribution and its presentation changes. It does not grant additional rights beyond those provided by the applicable source licenses.
