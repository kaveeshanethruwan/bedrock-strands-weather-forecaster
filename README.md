# Weather Forecaster

A Python-based AI agent that retrieves and explains weather forecasts using the National Weather Service API. Built with `strands-agents`.

## Features

- **Natural Language Interface**: Ask for weather information in plain English.
- **Real-time Data**: Fetches live data from the National Weather Service (NWS).
- **Intelligent Processing**: Formats and highlights key weather details (temperature, alerts, precipitation).

## Prerequisites

- Python 3.x

## Installation

1. Clone the repository (if applicable) or navigate to the project directory.
2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

Run the main script to query the weather agent:

```bash
python index.py
```

By default, the script asks: _"What's the weather like in Seattle?"_. You can modify the query in `index.py`.

## How it Works

The agent uses a system prompt to define its role as a weather assistant. It utilizes the `http_request` tool to interact with NWS API endpoints:

1. Resolves location to grid coordinates via `api.weather.gov/points`.
2. Fetches the forecast using the grid link.
3. Synthesizes the response into a user-friendly format.
