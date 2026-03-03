<div align="center">

# 📊 SmartPortfolio

**Intelligent Portfolio Optimization using Graph Neural Networks, Prophet Forecasting, and Deep Reinforcement Learning**

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

![Terminal UI Preview](https://img.shields.io/badge/Interface-Terminal%20TUI-orange)

</div>

---

## 🚀 Overview

SmartPortfolio is a terminal-based portfolio optimization system that combines cutting-edge machine learning techniques to generate intelligent asset allocations:

- **🔗 Graph Neural Networks (GAT)** — Model complex asset relationships and correlations
- **📈 Prophet Forecasting** — Time series predictions with seasonality awareness
- **🤖 Deep Reinforcement Learning (PPO)** — Dynamic allocation via hierarchical agents
- **💻 Neural Terminal TUI** — Beautiful, Bloomberg-inspired terminal interface

## ✨ Features

| Feature | Description |
|---------|-------------|
| **PyTorch GAT** | Pure PyTorch Graph Attention Network for asset embeddings |
| **Correlation Graphs** | Dynamic asset relationship visualization |
| **Live Prices** | Real-time market data via yfinance |
| **Portfolio Metrics** | Expected return, volatility, Sharpe ratio |
| **Plot Export** | Save allocation charts (pie, bar, dashboard) |
| **8GB RAM Optimized** | Memory-efficient for consumer hardware |

## 📦 Installation

### Prerequisites

- Python 3.10 or higher
- pip package manager

### Quick Install

```bash
# Clone the repository
git clone https://github.com/yourusername/smartportfolio.git
cd smartportfolio

# Create virtual environment
python -m venv .venv
.venv\Scripts\activate  # Windows
source .venv/bin/activate  # Linux/Mac

# Install package
pip install -e .
```

### Dependencies

Core dependencies are automatically installed:
- `torch` — PyTorch for neural networks
- `networkx` — Graph operations
- `prophet` — Time series forecasting
- `stable-baselines3` — Reinforcement learning
- `textual` — Terminal user interface
- `yfinance` — Market data

## 🎮 Usage

### Launch the TUI

```bash
# Start with default tickers
smartportfolio

# Start with custom ticker file
smartportfolio --tickers my_tickers.csv
```

### TUI Commands

| Command | Description |
|---------|-------------|
| `LOAD <file>` | Load tickers from CSV/XLSX file |
| `LOADWEIGHTS <file>` | Load previous portfolio weights |
| `RUN` | Execute optimization pipeline |
| `STATUS` | Show current system status |
| `EXPORT` | Export weights to CSV |
| `PLOT` | Save allocation charts |
| `GRAPH` | Save correlation graph visualization |
| `HELP` | Display help information |
| `CLEAR` | Reset all state |

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `q` | Quit application |
| `r` | Run optimization |
| `l` | Load tickers |
| `e` | Export results |
| `h` | Show help |
| `Esc` | Focus command bar |

### Ticker File Format

```csv
ticker
AAPL
MSFT
GOOGL
AMZN
META
```

## 📊 Output Files

All outputs are saved to the `outputs/` directory with timestamp-UUID naming:

| File Pattern | Description |
|--------------|-------------|
| `*_portfolio_weights.csv` | Asset weights allocation |
| `*_allocation_pie.png` | Pie chart visualization |
| `*_allocation_bar.png` | Bar chart visualization |
| `*_correlation_graph.png` | Asset relationship graph |
| `*_dashboard.png` | Combined metrics dashboard |

## 🏗️ Architecture

```
smartportfolio/
├── __init__.py          # Package initialization
├── __main__.py          # CLI entry point
├── app.py               # Main TUI application
├── config.py            # Configuration management
├── visualization.py     # Matplotlib plotting
├── data/                # Data handling modules
│   ├── fetcher.py       # Yahoo Finance data fetcher
│   ├── features.py      # Feature engineering
│   └── storage.py       # Local file storage
├── graph/               # Graph neural network modules
│   ├── builder.py       # Dynamic graph construction
│   ├── gat.py           # NumPy GAT implementation
│   └── torch_gat.py     # PyTorch GAT implementation
├── forecasting/         # Time series forecasting
│   └── prophet_model.py # Prophet integration
├── rl/                  # Reinforcement learning
│   ├── environment.py   # Gymnasium environment
│   └── agent.py         # PPO agent
└── components/          # TUI widgets
    ├── header.py        # App header
    ├── sidebar.py       # Watchlist sidebar
    └── main_content.py  # Portfolio overview
```

## 🔧 Configuration

Configuration is managed via `smartportfolio/config.py`:

```python
# Model parameters
gat_embedding_dim = 32
gat_num_heads = 4
gat_dropout = 0.1

# Data parameters
default_period = "2y"
correlation_threshold = 0.3

# RL parameters
rl_learning_rate = 0.0003
train_episodes = 100
```

## 🧪 Development

### Setup Development Environment

```bash
# Install with dev dependencies
pip install -e ".[dev]"

# Run tests
pytest

# Format code
black smartportfolio/

# Lint code
ruff check smartportfolio/
```

### Running Tests

```bash
pytest tests/ -v --cov=smartportfolio
```

## 📈 Performance

Tested on consumer hardware (8GB RAM):

| Operation | Time | Memory |
|-----------|------|--------|
| Data fetch (10 tickers) | ~5s | ~200MB |
| Graph construction | <1s | ~50MB |
| GAT embedding | ~2s | ~300MB |
| Full pipeline | ~15s | ~500MB |

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔐 Security

For security concerns, please see our [Security Policy](SECURITY.md).

## 📞 Support

- 📖 [Documentation](https://github.com/yourusername/smartportfolio#readme)
- 🐛 [Issue Tracker](https://github.com/yourusername/smartportfolio/issues)
- 💬 [Discussions](https://github.com/yourusername/smartportfolio/discussions)

## 🙏 Acknowledgments

- [Textual](https://github.com/Textualize/textual) — Terminal UI framework
- [Prophet](https://facebook.github.io/prophet/) — Time series forecasting
- [Stable-Baselines3](https://stable-baselines3.readthedocs.io/) — RL algorithms
- [yfinance](https://github.com/ranaroussi/yfinance) — Market data

---

<div align="center">

**Made with ❤️ by Anonymous**

</div>