# Ultimate DevOps Project Demo

This repository is a comprehensive demo application designed to showcase modern DevOps practices, observability, and microservices architecture using OpenTelemetry and related tools. It includes multiple services written in different languages, integrated with telemetry, monitoring, and tracing solutions.

## Features
- **Microservices Architecture:** Multiple services (accounting, ad, cart, checkout, currency, email, fraud, frontend, image provider, payment, product catalog, quote, recommendation, shipping, etc.)
- **Observability:** Integrated with OpenTelemetry Collector, Jaeger, Grafana, Prometheus, and Tracetest for distributed tracing and metrics.
- **Demo Platform:** Supports local development and deployment via Docker Compose and Kubernetes manifests.
- **Telemetry Components:** Includes configuration for OpenTelemetry Collector, resource attributes, and exporters.
- **Dependent Services:** Includes Kafka, Valkey, Flagd, and Flagd UI for feature flagging and messaging.
- **Load Generation:** Locust-based load generator for performance and stress testing.

## Getting Started

### Prerequisites
- Docker & Docker Compose
- (Optional) Kubernetes (for k8s manifests)
- Make

### Quick Start (Local)
1. Clone the repository:
   ```sh
   git clone <repo-url>
   cd ultimate-devops-project-demo-main
   ```
2. Build and start the demo using Docker Compose:
   ```sh
   docker-compose up --build
   ```
3. Access the frontend at [http://localhost:8080](http://localhost:8080)

### Kubernetes Deployment
Kubernetes manifests are available in the `kubernetes/` directory for deploying all services and dependencies.

## Project Structure
- `.env` — Environment variables for all services and dependencies
- `docker-compose.yml` — Main Docker Compose file
- `kubernetes/` — Kubernetes manifests for all services
- `src/` — Source code for each microservice
- `internal/` — Internal tools and scripts
- `test/` — Testing utilities

## Core Services
- **Accounting** (`src/accounting/`)
- **Ad** (`src/ad/`)
- **Cart** (`src/cart/`)
- **Checkout** (`src/checkout/`)
- **Currency** (`src/currency/`)
- **Email** (`src/email/`)
- **Fraud Detection** (`src/fraud-detection/`)
- **Frontend** (`src/frontend/`)
- **Frontend Proxy** (`src/frontend-proxy/`)
- **Image Provider** (`src/image-provider/`)
- **Load Generator** (`src/load-generator/`)
- **Payment** (`src/payment/`)
- **Product Catalog** (`src/product-catalog/`)
- **Quote** (`src/quote/`)
- **Recommendation** (`src/recommendation/`)
- **Shipping** (`src/shipping/`)

## Telemetry & Monitoring
- **OpenTelemetry Collector**
- **Jaeger**
- **Grafana**
- **Prometheus**
- **Tracetest**

## Dependent Services
- **Kafka**
- **Valkey**
- **Flagd**
- **Flagd UI**

## Environment Variables
All configuration is managed via the `.env` file. Key variables include image versions, service ports, addresses, and telemetry endpoints.

## Contributing
Contributions are welcome! Please see `CONTRIBUTING.md` for guidelines.

## License
This project is licensed under the MIT License. See `LICENSE` for details.

## Maintainers
- [OpenTelemetry Demo Team](https://github.com/open-telemetry)

---
For more details, refer to the documentation in each service's directory and the comments in `.env`.
