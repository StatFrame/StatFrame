# Changelog

All notable changes to the StatFrame application will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
- Early prototype for X-13ARIMA-SEATS integration in the Seasonal Adjustment module.

---

## [1.0.0] - 2026-06-06
### Added
- **Unified Workspace Interface:** RStudio-style desktop environment featuring a Data Explorer, Script Editor, and interactive Methodology Dashboard.
- **Administrative Data Mode:** New project configuration toggle that automatically adjusts the 11-module pipeline for longitudinal data vs. cross-sectional survey data.
- **Entity Linkage Module:** Integrated `splink` (DuckDB backend) for high-performance business register demographic tracking (mergers, deaths, ID changes).
- **Diagnostic Reports:** Module-level "Traffic Light" warning system to alert users of dangerous methodological thresholds.
- **Variance due to Imputation:** Added robust Winsorized analytical residual calculation to protect against explosive variance from skewed enterprise data.

### Changed
- Rebranded application from NovaSurvey to StatFrame to better reflect enterprise statistical production capabilities.
- Switched distribution model exclusively to zero-install, portable `.zip` archives for air-gapped security compliance.
- Removed legacy CLI integration from the public interface; all workflows now route through the Command Center GUI.

### Fixed
- Resolved UI freezing when rendering administrative datasets larger than 10 million rows by implementing Polars `LazyFrame` pagination in the Data Glimpse viewer.
