# Energy Visualization Tools

## Overview
This project provides a suite of visualization tools for analyzing energy consumption and flow patterns across the United States. Developed by the Laboratory for Intelligent Integrated Networks of Engineering Systems at Stevens Institute of Technology, these tools enable temporal analysis through various visualization methods including Sankey diagrams, network flow maps, and choropleth maps.

## Authors
- Hazem Abo-Donia
- Amro M. Farid

Laboratory for Intelligent Integrated Networks of Engineering Systems, Stevens Institute of Technology

## Acknowledgement
This research was generously funded by the United States National Science Foundation.

## Installation

### Prerequisites
- Python 3.x
- pip (Python package installer)

### Dependencies
Install all required dependencies using:
```bash
pip install -r requirements.txt
```

Required packages include:
- geopandas
- matplotlib
- pandas
- plotly
- networkx
- ipywidgets
- ipympl

## Features

### 1. Temporal Sankey Diagram (`visualizeTemporalSankeyDiagram`)
- Visualizes energy flow between different nodes over time
- Interactive yearly slider for temporal analysis
- Custom color-coding for different energy sources/sinks
- Requires input CSV with columns: source, target, value, year

### 2. Temporal Network Flow Map (`visualizeTemporalNetworkFlow`)
- Displays energy flow patterns between US states
- Dynamic visualization with temporal slider
- Color-coded flow magnitude
- Requires input CSV with columns: state1, state2, magnitude, Year

### 3. Temporal Choropleth Map (`visualizeTemporalChoroplethMap`)
- Shows state-wise energy usage patterns over time
- Interactive temporal slider
- Color gradient indicating energy usage intensity
- Requires input CSV with columns: state_name, time_step (YYYYMM format), energy_usage

## Usage

### Temporal Sankey Diagram
```python
visualizeTemporalSankeyDiagram('path_to_your_sankey_data.csv')
```

### Temporal Network Flow Map
```python
visualizeTemporalNetworkFlow('path_to_your_network_data.csv')
```

### Temporal Choropleth Map
```python
visualizeTemporalChoroplethMap('path_to_your_choropleth_data.csv')
```

## Data Format Requirements

### Sankey Diagram Data
```csv
source,target,value,year
NodeA,NodeB,100,2020
NodeB,NodeC,50,2020
...
```

### Network Flow Data
```csv
state1,state2,magnitude,Year
New York,New Jersey,150,2020
California,Nevada,200,2020
...
```

### Choropleth Map Data
```csv
state_name,time_step,energy_usage
New York,202001,1500
California,202001,2000
...
```

## Error Handling
Each visualization function includes comprehensive error handling and returns:
- `True` for successful visualization
- `False` with error message for failed attempts

## License
Copyright (c) 2023-2024 Laboratory for Intelligent Integrated Networks of Engineering Systems

## Contact
Laboratory for Intelligent Integrated Networks of Engineering Systems
Stevens Institute of Technology