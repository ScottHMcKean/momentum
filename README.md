# Momentum Trading Strategy

A data-driven momentum trading system designed to identify and capitalize on short-term price movements with 1-3 day holding periods.

## Project Intent

This project combines simple, tested algorithms with fundamental analysis to build a lower-risk momentum trading strategy. Key features include:

- **Short-term momentum detection** with 1-3 day holding periods
- **Automated data ingestion** using Lakeflow to sync stock data from Yahoo Finance
- **Backtesting framework** for strategy validation and risk assessment
- **Production-ready deployment** using Databricks Asset Bundles for CI/CD
- **Real money trading pipeline** (once strategy is validated through backtesting)

## Technology Stack

- **Databricks** for data processing and model execution
- **Lakeflow** for automated stock data synchronization
- **Asset Bundles** for CI/CD and deployment automation
- **Databricks Connect** for local development and testing
- **UV** for Python dependency management

## Getting Started

1. **Prerequisites**: Install [UV](https://docs.astral.sh/uv/getting-started/installation/) and [Databricks CLI](https://docs.databricks.com/dev-tools/cli/databricks-cli.html)

2. **Authentication**: Configure Databricks CLI
   ```bash
   databricks configure
   ```

3. **Local Development**: Install dependencies and run tests
   ```bash
   uv sync
   uv run pytest
   ```

4. **Deploy to Databricks**:
   ```bash
   # Development environment
   databricks bundle deploy --target dev
   
   # Production environment  
   databricks bundle deploy --target prod
   ```

5. **Run the pipeline**:
   ```bash
   databricks bundle run
   ```

## Development

This project follows modular design principles optimized for Databricks deployment. Tests use real integrations where possible and avoid mocks for faster, more reliable validation.
