# EONET — NASA Earth Natural Events Dashboard

An interactive Python notebook that visualises real-time natural events (wildfires, storms, volcanoes, icebergs, and more) using the [NASA EONET v3 API](https://eonet.gsfc.nasa.gov/docs/v3), with a wildfire deep dive and long-term climate change tracking from [NASA GISS](https://data.giss.nasa.gov/gistemp/) and [NOAA](https://gml.noaa.gov/ccgg/trends/).

## Prerequisites

- Python 3.12+ (tested with 3.12)

## Setup

```bash
# 1. Clone the repo
git clone <repo-url>
cd eonet

# 2. Create a virtual environment with the latest Python
python3 -m venv .venv

# 3. Activate the virtual environment
source .venv/bin/activate        # macOS / Linux
# .venv\Scripts\activate         # Windows

# 4. Install dependencies
pip install -r requirements.txt
```

## Usage

Open `eonet_dashboard.ipynb` in VS Code (or Jupyter) and **Run All** cells. No API key is required — all data sources are open and free.

## What's Inside

### Natural Events (EONET)

| Section | Description |
|---------|-------------|
| World map | Colour-coded scatter map of recent events |
| Treemap & bar chart | Event distribution by category |
| Weekly timeline | Stacked area chart of activity over time |
| Open vs Closed | Monthly breakdown of event status |
| Longest-running events | Top 15 open events by days active |
| Magnitude analysis | Scatter + box plot for events with magnitude data |
| Hotspot heatmap | Density map showing geographic clusters |
| Day × Hour heatmap | Reporting patterns by day-of-week and UTC hour |

### Wildfire Deep Dive

| Section | Description |
|---------|-------------|
| Summary cards | Total fires, still burning, earliest & most recent dates |
| Gantt timeline | Top 40 longest-burning fires with start/end dates |
| Seasonality | Which months see the most wildfire starts |
| Weekly activity | New fires per week + cumulative total |
| Animated map | Monthly time-slider showing fire locations globally |
| Fire table | Every wildfire with start date, end date, and duration |

### Climate Change Tracking

| Section | Description |
|---------|-------------|
| Temperature anomaly | NASA GISTEMP v4 monthly data (1880–present) with 12-month rolling average and trend line |
| Warming by decade | Average anomaly per decade, blue→red colour scale |
| Keeling Curve | Atmospheric CO₂ at Mauna Loa (1958–present) with 350/400 ppm milestones |
| Temp vs CO₂ | Dual-axis annual chart + Pearson correlation |
| Warming rate | Decade-over-decade acceleration + CO₂ vs temperature scatter with OLS trendline |

## Data Sources

- [NASA EONET v3 API](https://eonet.gsfc.nasa.gov/api/v3/events) — Earth Observatory Natural Event Tracker
- [NASA GISS GISTEMP v4](https://data.giss.nasa.gov/gistemp/) — Global Surface Temperature Analysis
- [NOAA GML](https://gml.noaa.gov/ccgg/trends/) — Mauna Loa CO₂ (Keeling Curve)