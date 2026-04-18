# Agents

A fork of [Polymarket/agents](https://github.com/Polymarket/agents) — autonomous trading agents for Polymarket prediction markets.

## Overview

This project provides a framework for building and running automated agents that interact with Polymarket prediction markets. Agents can analyze market data, make predictions, and execute trades based on configurable strategies.

## Features

- Autonomous market analysis and trading
- Configurable agent strategies
- Integration with Polymarket API
- Docker support for deployment

## Requirements

- Python 3.10+
- Docker (optional)

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/your-org/agents.git
cd agents
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure environment

```bash
cp .env.example .env
# Edit .env with your credentials
```

### 4. Run an agent

```bash
python -m agents.main
```

## Docker

```bash
docker build -t agents .
docker run --env-file .env agents
```

## Configuration

See `.env.example` for all available environment variables.

> **Personal note:** I've been testing with `TRADE_INTERVAL=300` (5 minutes) and `MAX_POSITION_SIZE=10` USDC as conservative defaults while learning the system. Recommend starting low.
>
> Also useful: set `DRY_RUN=true` to simulate trades without actually submitting orders — good for sanity-checking a new strategy before going live.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

MIT
