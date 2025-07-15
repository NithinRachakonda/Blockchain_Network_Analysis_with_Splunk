# Blockchain Network Monitoring with Splunk
This project presents a real-time Bitcoin transaction monitoring system using **Splunk**. The core objective is to identify suspicious patterns by analyzing live transaction streams and profiling address behavior for potential fraud detection.

## Project Highlights
- **Live Data Streaming**: 
  Ingests real-time unconfirmed Bitcoin transactions using the [Blockchain WebSocket API](https://www.blockchain.com/explorer/api/api_websocket).
- **Splunk Integration**: 
  Uses HTTP Event Collector (HEC) to stream data directly into Splunk for analysis and visualization.
- **Fraud Analysis Dashboards**:
  Two key dashboards were created:
  - **Transaction Volume Analysis**: Tracks total volume, average value, size distribution, and frequency over time.
  - **Address Activity Analysis**: Highlights the top 10 sender/receiver addresses and total Bitcoin sent/received.

## Repository Contents

| File | Description |
|------|-------------|
| `bitcoin_stream_to_splunk.py` | Python script to pull live BTC transactions and forward selected fields to Splunk |
| `Memo.pdf` | Details on Splunk dashboards and key metrics used for fraud analysis |
| `Data.pdf` | Overview of the data ingested from Blockchain's WebSocket API |
| `Market_Analysis.pdf` | Dashboard visualizing transaction size distribution and volume |
| `Investment_Performance.pdf` | Dashboard profiling transactional behavior of BTC addresses |

## How It Works

1. **Run the Python script** to connect to the Blockchain WebSocket API and stream live unconfirmed transactions.
2. **Filter and forward relevant fields** (timestamp, sender/receiver address, transaction size, value) to Splunk using the HEC endpoint.
3. **Visualize** the incoming data with custom-built dashboards on:
   - Top sending/receiving addresses
   - Total and average transaction values
   - Anomalous patterns indicating potential fraud

## 🛠Setup Requirements
- Python 3.8+
- `requests` and `websocket-client` libraries
- A running Splunk instance with HEC enabled

## 📎 References
- [Blockchain WebSocket API](https://www.blockchain.com/explorer/api/api_websocket)

> This project was built to explore the use of **real-time data pipelines** for blockchain transaction monitoring. It demonstrates how streaming data can drive meaningful **security and financial insights** when combined with powerful visualization tools like Splunk.
