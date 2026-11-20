# AWS Server Monitoring using Prometheus and Grafana

## Project Overview
This project implements a server monitoring system on an AWS EC2 instance using Docker, Prometheus, Grafana, and Node Exporter.

It collects system-level metrics and displays them through Grafana dashboards.

## Architecture

AWS EC2 Instance
       |
   Docker Compose
       |
  -------------------------
  |          |            |
Prometheus  Grafana   Node Exporter
  |          |
  |------ Metrics -------|

## Technologies Used
- AWS EC2
- Amazon Linux 2023
- Docker
- Docker Compose
- Prometheus
- Grafana
- Node Exporter
- Linux
- YAML

## Services and Ports

| Service | Port | Purpose |
|---------|------|---------|
| Prometheus | 9090 | Metrics collection |
| Grafana | 3000 | Metrics visualization |
| Node Exporter | 9100 | System metrics |

## Setup Instructions

1. Clone this repository:

   git clone https://github.com/vithikamishra512/aws-server-monitoring.git

2. Navigate to the project directory:

   cd aws-server-monitoring

3. Start the monitoring services:

   docker compose up -d

4. Check running containers:

   docker ps

## Access Services

- Prometheus: http://YOUR-EC2-PUBLIC-IP:9090
- Grafana: http://YOUR-EC2-PUBLIC-IP:3000

## Security Notes
- Do not upload .env files, passwords, SSH keys, or other credentials.
- Configure your own SMTP credentials locally if email notifications are required.
- Restrict AWS security group access to trusted IP addresses.

## Learning Outcomes
- Deployed a monitoring stack on AWS EC2.
- Configured Prometheus to scrape metrics.
- Used Node Exporter for system monitoring.
- Visualized monitoring data using Grafana.
- Managed multiple containers using Docker Compose.
