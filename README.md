Failure Puzzle – Chaos Engineering with Online Boutique

This project is a fork of Google’s Online Boutique demo application, adapted to explore chaos engineering and modern observability practices.

Purpose

While the original Online Boutique demonstrates cloud-first microservices on GKE (and other Kubernetes clusters), this fork introduces controlled chaos injection to:

Break specific dependencies (network partitions, service crashes, latency injection).

Observe how the system behaves under stress and partial failure.

Highlight how resilience patterns, retries, and fallbacks work in practice.

Provide developers with hands-on experience debugging distributed systems in failure conditions.

What’s New in This Fork

Compared to the upstream Google project, we extend the demo with:

Chaos experiments: automated injection of failures into microservices to simulate real-world outages.

OpenTelemetry Collector integration: routes telemetry to OpenSearch
 via Data Prepper for deep trace and metrics analysis.

Dashboards for observability: OpenSearch Dashboards preconfigured to visualize trace analytics, service maps, and performance bottlenecks.

Helm-based setup: simplified deployment of observability stack (OpenSearch, Dashboards, Data Prepper, OTel Collector).

Failure Puzzle workflows: experiments designed to progressively “puzzle” the system, forcing you to trace symptoms back to root causes.

Base Project

We build on Google’s Online Boutique:

11 microservices in different languages (Go, Java, Python, Node.js, C#).

Standard e-commerce flows: browse, cart, checkout, payment, shipping, ads, and recommendations.

Works on GKE, Minikube, Kind, or other Kubernetes clusters.

Getting Started

(Todo I'll fill in screenshots and examples later)

Deploy the base Online Boutique application as usual.

Deploy the observability stack via Helm (OpenSearch, Data Prepper, OTel Collector).

Enable chaos experiments to start injecting controlled failures.

Observe trace data and metrics in OpenSearch Dashboards.