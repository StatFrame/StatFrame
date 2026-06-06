# 🌿 StatFrame

**StatFrame is an end-to-end statistical production platform designed to process, analyze, and publish high-quality survey and administrative data.**

Built to mirror the rigorous data pipelines of national statistical offices, StatFrame bridges the gap between deep methodological engineering and subject matter expertise. It automates complex, heavy-lifting statistical procedures—such as longitudinal editing, multi-method imputation, calibration, and total variance estimation—allowing both methodologists and operational analysts to build production-grade official statistics pipelines without writing complex mathematical code from scratch.

StatFrame focuses exclusively on processing and estimation. It assumes you already have your data; **it contains no data collection tools.**

---

## ✨ Core Capabilities

StatFrame is structured around a modular, unified data pipeline consisting of specialized statistical components that adapt dynamically to your project type (Survey vs. Administrative Census):

### 🔄 Ingestion & Linkage
- **Survey Ingestion & Profiling:** Automated structural validation and initial data profiling.
- **Record Linkage & Demographics:** High-performance entity resolution to track business register dynamics, including mergers, acquisitions, split-offs, deaths, and ID changes over time.

### 🧹 Data Cleaning & Processing
- **Data Editing & Outliers:** Cross-sectional outlier detection for surveys alongside longitudinal historical rule checking for monthly administrative data.
- **Missing Data Imputation:** Advanced donor/regression imputation for surveys, paired with historical tracking models (LOCF, trend, and YoY ratios) for administrative census records.
- **Variance due to Imputation:** Automatic quantification of the statistical uncertainty introduced by imputation passes to safeguard against artificial precision.

### ⚖️ Estimation & Weighting
- **Influential Unit Treatment:** Targeted identification and containment of extreme records before macro-aggregation.
- **Non-Response Weighting & Calibration:** Complex grossing-up procedures, raking, and benchmarking to known administrative or population totals.
- **Total Variance Estimation:** Comprehensive pooling of sampling and imputation variance components to calculate true coefficients of variation ($CV$).

### 📈 Advanced Analytics & Publishing
- **Small Area Estimation (SAE):** Model-based domain estimation for sparse data subpopulations.
- **Seasonal Adjustment:** Time-series decomposition for monthly and quarterly production runs.
- **Statistical Disclosure Control (SDC):** Automated data masking, suppression, and micro-data protection prior to dissemination.

---

## 🚀 The StatFrame Workflow

StatFrame operates on a **Unified Workspace** concept:

1. **Initialize Project:** Choose between a *Cross-Sectional Survey* or a *Longitudinal Administrative Data* pipeline. The workspace automatically adapts its underlying toolkit.
2. **Import Data:** Point the high-performance computational engine to your local files (optimized for Parquet and CSV scales of tens of millions of records).
3. **Configure & Run:** Set automated data-driven guardrails using the interactive dashboard, or utilize the integrated script editor for custom programmatic control.
4. **Evaluate Quality:** Review module-level Diagnostic Impact Statements, traffic-light warning thresholds, and data continuity dashboards.
5. **Secure & Publish:** Apply disclosure controls and generate reproducible, publication-ready data products.

---

## 📁 Ecosystem & Repository Structure

The StatFrame platform is distributed across a multi-repository architecture. You are currently viewing the public face of the project.

### 🌍 Public Repositories
- **[`StatFrame`](https://github.com/StatFrame/StatFrame):** (This Repository) The central hub for the platform. It contains the public issue tracker, feature request discussions, and the official release binaries (available in the **Releases** tab as portable `.zip` archives).
- **[`docs`](https://github.com/StatFrame/docs):** The source repository for our official user guides, onboarding tutorials, and integration instructions.

### 🔒 Proprietary Core Repositories (Private)
The underlying architecture driving the StatFrame releases is maintained in private enterprise repositories:
- **`engine`:** The high-performance computational backend (Polars/Rust) and data processing pipeline orchestration.
- **`core`:** The proprietary methodological algorithms (Editing, Imputation, SAE, SDC, etc.) and mathematical frameworks.

---

## 🖥️ Interfaces & Environments

StatFrame is distributed as a zero-install, self-contained desktop environment designed for maximum security, portability, and ease of use.

- 📦 **Zero-Install Portability:** Distributed entirely as a portable `.zip` archive. There are no installer wizards, no single `.exe` setups, and no administrator privileges required. Simply extract the folder and launch the application—perfect for strict corporate or government IT environments.
- 🖱️ **The Unified Workspace (GUI):** A comprehensive, integrated development environment (IDE) built for statistics. Similar to RStudio, it combines your data explorer, script editor, console output, and visual methodology dashboards into a single, cohesive window.
- 📁 **Portable Projects (.sfproj):** Fully self-contained, reproducible statistical environments capturing data references, pipeline metadata, and script state. You can zip a project folder and share it with a colleague, ensuring perfect reproducibility.

---

## 🧠 Philosophy

StatFrame is built on a central principle:

> Statistical complexity should not block access to insights, nor should simplicity compromise mathematical rigor.

The platform ensures that administrative or survey operations remain audit-ready, completely transparent, and scientifically sound—regardless of the technical programming background of the subject matter expert running the system.

---

## 🔐 License

- **StatFrame Software:** The compiled binaries and releases distributed in this repository are proprietary and licensed under the StatFrame End User License Agreement (see the `LICENSE` file attached to releases).
- **Documentation:** All markdown documentation files, guides, and visual assets are licensed under Creative Commons Attribution 4.0 International (`CC BY 4.0`).
- **Code Examples:** Any integration templates, pipeline configuration JSONs, or custom validation snippets are openly licensed under the `MIT License`.

---

## 🛠️ Project Status

This platform is actively under development. Expect frequent updates, continuous API stability refinements, and expanding core methodological modules.
