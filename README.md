# Live-Network-Traffic-Analyzer
This project was completed as a part of the ICCS492: The Guts of Modern System course by Kanladaporn Sirithatthamrong, Phavarisa Limchitti and Tath Kanchanarin.

## Overview

The **Live Network Traffic Analyzer** is designed to process, enrich, and visualize network traffic data in real-time. The tool aims to summarize traffic flow, including information such as:

- **Countries** the traffic originates from and travels to
- **Autonomous Systems (AS)** involved in the traffic flow
- **Traffic Volume** per country and per AS

### Key Features

- **Flow Enrichment**: Augments NetFlow/IPFIX data with additional metadata such as origin country, destination country, and AS details using publicly available CIDR and AS datasets.
- **Data Storage**: Time-series database to store enriched flow data, enabling retrospective analysis within a 24-hour period.
- **Interactive Dashboard**: Provides visual analytics for the user, showing historical traffic statistics, adjustable for specific time ranges.

### Technologies

- **Programming Language**: Rust (for multithreading efficiency)
- **Flow Protocols**: NetFlow v5 and IPFIX
- **Datasets**: 
  - IP block to country mapping: [GitHub - country-ip-blocks](https://github.com/herrbischoff/country-ip-blocks)
  - IP to Autonomous System mapping: [IPtoASN](https://iptoasn.com/)

### Project Components

1. **Flow Collector**: Captures NetFlow/IPFIX data.
2. **Data Enricher**: Processes flow data to append geographical and AS information.
3. **Data Store**: Stores time-series data for later querying and visualization.
4. **Dashboard**: Interactive frontend for data visualization and analytics.

### Usage

1. Run the flow collector to capture traffic.
2. The data enricher program will augment the traffic data.
3. View historical traffic on the interactive dashboard.
