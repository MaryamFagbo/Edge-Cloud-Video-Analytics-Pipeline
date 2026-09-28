
# Distributed Vision Analytics and Split Inference Framework

A lightweight, self-contained Python simulation modeling a distributed edge-cloud architecture that dynamically partitions deep neural network layers based on real-time network volatility and hardware telemetry.

---

Maryam Fagbo

## Overview

In modern distributed vision systems and resource-constrained nodes, executing heavy pipelines entirely on edge hardware causes thermal throttling, while pushing raw streams to the cloud incurs severe bandwidth overhead. This project implements:
1. **Adaptive Telemetry Monitoring:** Simulates fluctuating wireless throughput (Mbps) alongside edge processor workload utilization.
2. **Dynamic Strategy Offloading:** Automatically decides whether to process frames locally, execute split-layer feature extraction, or migrate payloads entirely to a cloud infrastructure.
3. **Multi-Tier Performance Analytics:** Generates time-series visualization charts tracking system resource stress against end-to-end processing latency.

---

## How to Run

You can view and execute this notebook directly in your browser using Google Colab:
[![Open In Colab]: https://colab.research.google.com/drive/111AMYCC6E6NjFLrW7uWqks8ynwALTYM8?usp=sharing
## Code Architecture

* **Dependencies:** `numpy`, `matplotlib`
* **Core Paradigm:** Policy-driven dynamic task offloading across a distributed node topology.
* **Execution Environment:** Designed for rapid prototyping and validation in Google Colab or standard local Python environments.

```python
# Core offloading decision logic snippet
if load > 90.0 or bw < 3.0:
    strategy = 0  # Local Edge Processing
elif 3.0 <= bw < 18.0:
    strategy = 1  # Split-Layer Offloading (Intermediate Tensors)
else:
    strategy = 2  # Full Cloud Migration
________________________________


    
