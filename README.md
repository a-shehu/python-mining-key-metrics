🐍  # python-mining-key-metrics
[![Python](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Panel](https://img.shields.io/badge/Panel-1.4-lightgrey)](https://panel.holoviz.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Interactive visualization dashboard in Python with [Panel](https://panel.holoviz.org/).

This repository contains code for a portfolio project showcasing an interactive dashboard built with Panel.
If you want to see all the dependencies for this project, please refer to the `requirements.txt` file.

## Overview

This project simulates Bitcoin mining metrics based on varying power consumption (MW). It produces realistic outputs reflecting mining performance, efficiency, network parameters, and economics, all driven by industry benchmarks around 2025.

### 🚀 How to Run

To serve the dashboard locally, open a terminal and run the following command:

```bash
panel serve asic-data-interact.ipynb --port 5010 --show --port 5010 --show
```

## Model Structure

- Generates data for MW values from 1 up to a configurable max (slider²).
- Calculates key metrics such as hashrate, energy use, BTC production, fees, latency, and ASIC utilization.
- Reflects realistic scaling and diminishing returns trends.

## Key Metrics Summary

| Metric                         | Behavior with MW                              |
|--------------------------------|----------------------------------------------|
| Total Hashrate (PH/s)          | Constant (1500 PH/s)                          |
| BTC Production (BTC/day)       | Increases with √MW (slow growth)              |
| Energy Consumption (MWh/day)   | Linear with MW                                |
| Energy Efficiency (BTC/MW)     | Decreases as MW increases (diminishing returns) |
| Transaction Fees (BTC)         | Increases slightly faster than linear         |
| Transaction Latency (s)        | Decreases with MW, minimum 1 second           |
| ASIC Utilization (%)           | Increases gradually with MW                   |

## Usage

1. Run the Panel app or notebook.
2. Adjust the power slider (actual MW = slider squared).
3. Observe dynamically updated charts and table.
4. Export the dataset as CSV for offline analysis.

## Requirements

- Python 3.7+
- panel
- pandas
- numpy
- hvplot
- holoviews

Install dependencies via pip

```bash
pip freeze > requirements.txt
```



