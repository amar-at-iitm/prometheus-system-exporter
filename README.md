# prometheus-system-exporter: 

## Overview
This assignment focuses on building an AI application with Prometheus instrumentation. The objective is to collect system-level metrics (CPU, memory, and disk IO statistics) and expose them via a custom exporter. The Prometheus server is then configured to scrape and monitor these metrics.

## File Structure
```
Assignment6/
│-- system_metrics_exporter.py  # Python script to collect and expose system metrics
│-- prometheus.yml  # Prometheus configuration file
│-- README.md  # Readme file explaining the assignment
│-- documentation.pdf  # Detailed documentation of the implementation
```

## Files and Their Purpose
- **`system_metrics_exporter.py`**: A Python script that collects disk IO, CPU, and memory statistics and exposes them as Prometheus metrics.
- **`prometheus.yml`**: The configuration file for Prometheus to scrape the metrics at 2-second intervals.
- **`README.md`**: A concise explanation of the project, setup instructions, and usage.
- **`documentation.pdf`**: A detailed explanation of the project implementation, methodology, and results.

## Installation and Setup
### Prerequisites
- Python 3.x
- Prometheus installed and configured
- `psutil` and `prometheus_client` Python libraries

### Steps to Run the Exporter
1. Clone the repository:
   ```bash
   git clone https://github.com/DA5402-MLOps-JanMay2025/assignment-06-amar-at-iitm
   cd assignment-06-amar-at-iitm
   ```
2. Install dependencies:
   ```bash
   pip install psutil prometheus_client
   ```
3. Start the Prometheus metrics exporter:
   ```bash
   python system_metrics_exporter.py
   ```
4. Verify that metrics are available at:
   ```
   http://localhost:18000/metrics
   ```

### Running Prometheus Server
1. Move the `prometheus.yml` file to the Prometheus folder and start Prometheus with the provided `prometheus.yml` configuration:
   ```bash
   ./prometheus --config.file=prometheus.yml
   ```
2. Open Prometheus UI at:
   ```
   http://localhost:9090
   ```
3. Query metrics such as `io_read_rate` or `cpu_avg_percent`.

## Logging Mechanism
Logging is implemented at each step to ensure proper debugging and monitoring. Errors and successful data collections are logged.

