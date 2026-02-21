# Network Dashboards for Grafana

> **Work in progress.** These dashboards are under active development. Layouts, panel queries, and field references may change without notice.

Grafana dashboards for monitoring network traffic and protocols. Designed for use with an Elasticsearch backend datasource and data collected by standard Elastic Agent integrations (Fleet-managed).

## Dashboards

| ID | Title | Description |
|---|---|---|
| NT-00 | Network Overview | Top talkers, protocol distribution, traffic volume |
| NT-01 | Network Traffic | Flow-level traffic analysis with source/destination breakdown |
| NT-02 | DNS | DNS query volume, response codes, top domains |
| NT-03 | TLS Encryption | TLS versions, cipher suites, certificate details |
| NT-04 | Infrastructure Traffic | Service-specific traffic for Elasticsearch, Grafana, Fleet |
| NT-05 | NetFlow Analytics | NetFlow/IPFIX collector data with flow-level analysis |

## Data Sources

These dashboards use template variables for datasource selection, so they work with any Elasticsearch datasource name or UID. The expected data comes from:

- **Elastic Agent** `network_traffic` integration (packet capture and flow data)
- **NetFlow** integration (for NT-05 only — NetFlow/IPFIX/sFlow collector data)

## Installation

Copy the JSON files from `dashboards/` into Grafana via the UI import, the HTTP API, or the [grafana-dashboards-role](https://github.com/Oddly/grafana-dashboards-role) Ansible role.
