# Kickoff Football Data Lakehouse

Kickoff Football Data Lakehouse is a Databricks-based data engineering project focused on building a scalable lakehouse architecture for football data using PySpark. The project demonstrates modern cloud-native data engineering practices, including API integration, schema definition, and multi-layered data transformation workflows.

## Overview

The platform ingests football team and match data from the Football Data API, leveraging a secure token stored in a `.env` file at the project root. Data is retrieved using Python and requests, then processed and structured with PySpark in Databricks notebooks. The workflow follows a lakehouse approach, organizing data into bronze (raw), silver (cleansed), and gold (aggregated) stages, enabling unified analytics and governance.

## Key Features

- **Lakehouse Architecture:** Implements a unified data platform combining the reliability of data lakes with the performance of data warehouses, using Databricks and PySpark.
- **Cloud-Native Design:** Built for Databricks, enabling distributed data processing and seamless integration with cloud storage.
- **API Integration:** Securely fetches data from the Football Data API using a token loaded from environment variables.
- **PySpark Workflows:** Utilizes PySpark for schema definition, data ingestion, transformation, and storage.
- **Layered Data Modeling:** Employs bronze, silver, and gold data layers for progressive data refinement and analytics.
- **Job and Dashboard Automation:** Includes Databricks job and dashboard configurations for workflow orchestration and visualization.

## Technical Highlights

- **Environment Management:** Uses `python-dotenv` to manage sensitive credentials, ensuring secure API access.
- **Schema Definition:** Employs detailed PySpark schemas to enforce data structure and integrity.
- **Lakehouse Storage:** Writes processed data to Databricks tables, supporting scalable analytics and reporting within the lakehouse paradigm.
- **Notebook-Driven Development:** All workflows are implemented as Databricks notebooks, facilitating interactive development and collaboration.

## Security

API tokens are managed via a `.env` file with the key `FOOTBALLDATA_TOKEN`, ensuring credentials are not hardcoded and remain outside source control.