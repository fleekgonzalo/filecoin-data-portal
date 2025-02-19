# 🗂️ Filecoin Data Portal

[![CI](https://github.com/davidgasquez/filecoin-data-portal/actions/workflows/ci.yml/badge.svg)](https://github.com/davidgasquez/filecoin-data-portal/actions/workflows/ci.yml)

Open source, serverless, and local-first Data Platform for the Filecoin ecosystem. This data hub improves data access and empower collaboration within the community allowing users to spend more time on novel analysis and less time on data preparation!

![DAG](https://github.com/davidgasquez/filecoin-data-portal/assets/1682202/64d6adea-48d2-4cee-b0a2-b94bee733c14)

Check out the [Filecoin Data Portal](https://filecoin-data-portal.on-fleek.app/) website for dashboards and reports!

## 📂 Data

You can get the latest data a Parquet files from IPFS. The data lives under the [IPFS CID](https://raw.githubusercontent.com/davidgasquez/filecoin-data-portal/main/data/IPFS_CID) pointer available in this repository and at the IPNS address [`ipns://k51qzi5uqu5dktj2z0c6k27rxtpn2d4psdx4ph9p6481axcfn5iel2a7qehr3v`](https://ipfs.io/ipns/k51qzi5uqu5dktj2z0c6k27rxtpn2d4psdx4ph9p6481axcfn5iel2a7qehr3v/)

## 📖 Overview

This repository contains code and artifacts to help anyone process Filecoin data from [diverse sources](portal/docs/data-sources.md) (on-chain and off-chain). It is an implementation of [Datadex](https://github.com/davidgasquez/datadex), allowing anyone to collaborate on data, models, and pipelines in a permissionless way.

### 📦 Key Features

- **Open**
  - All code and data are open source.
  - Utilizes open standards and formats within the Arrow ecosystem.
- **Permissionless Collaboration**
  - Collaborate on data, models, and pipelines like Dune, but with open-source freedom.
  - No constraints from private APIs or platform lock-ins.
  - Enjoy full Git features such as branching, merging, and pull requests.
- **Decentralization Options**
  - Run the project on a laptop, server, CI runner, or even on decentralized compute networks like Bacalhau.
  - No local setup required; it even works seamlessly in GitHub Codespaces.
  - Data is stored in IPFS, where datasets will become more distributed as more users run it.
  - Multiple data sources and flexible exposure options.
- **Data as Code**
  - Each commit generates and pushes all table files to IPFS.
  - Easily access historical data snapshots.
  - Declarative and stateless transformations tracked in git.
  - Static dashboards and reports available at the [Filecoin Data Portal](https://filecoin-data-portal.on-fleek.app/).
- **Modular Flexibility**
  - Replace, extend, or remove individual components.
  - Works across various environments (laptop, cluster, browser).
  - Compatible with tons of tools. At the end of the day, tables are Parquet/CSV files.
- **Low Friction Data Usage**
  - Raw and processed data is available to anyone on IPFS. Use wathever tool you want!
  - Get started with simple actions like pasting a [SQL query in your browser](https://shell.duckdb.org/) or using `pd.read_parquet(url)` in a Notebook.
  - [Static Quarto Notebooks with embedded datasets](https://filecoin-data-portal.on-fleek.app/reports/2023-06-21-Exploring-Filecoin-Deals.html) are generated with every commit, serving as documentation or a simple reporting/dashboarding layer.
- **Modern Data Engineering**
  - Supports data engineering essentials such as typing, testing, materialized views, and development branches.
  - Utilizes best practices, including declarative transformations, and utilizes state-of-the-art tools like DuckDB.

## 💻 Getting Started

The easiest way to get started is to use Visuel Studio Code and rely on the Development Container configuration provided in this repository. Alternatively, you can install the dependencies locally or reuse the Dockerfile provided.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/davidgasquez/filecoin-data-platform)

You'll need the following secrets in your environment:

- A `SPACESCOPE_TOKEN` to access [Spacescope](https://spacescope.io/) API.

## 🛠️ Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. There are multiple interesting ways to contribute to this project:

- Add new data sources!
- Improve [dbt project](dbt/) models.
- Write a one off [report](reports/).
- Build a [dashboard](dashboards/).

## 📝 License

[MIT](https://choosealicense.com/licenses/mit/)
