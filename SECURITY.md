# Security Policy

At StatFrame, we take the security of statistical production environments and sensitive administrative data very seriously.

## 🛡️ Our Security Posture: Local-First & Air-Gapped
StatFrame is designed specifically for highly secure, restricted IT environments:
- **Zero Telemetry:** StatFrame does not send usage data, crash logs, or telemetry to any external servers.
- **Zero Cloud Processing:** All data processing, including memory-intensive record linkage and imputation, is performed 100% locally on your host machine.
- **Air-Gap Ready:** The portable `.zip` distribution requires no internet connection to install, run, or authenticate, making it safe for air-gapped workstations.

## Supported Versions

We currently provide security updates for the following versions of StatFrame. We strongly recommend always running the latest release.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

Please **do not** report security vulnerabilities through public GitHub issues. 

If you discover a vulnerability or a potential data-leakage issue within the application framework, please report it privately to our security team:

**Email:** [security@statframe.ca]

### What to include:
* StatFrame version and OS.
* A description of the vulnerability.
* Steps to reproduce the issue.

### Our Response:
We aim to acknowledge receipt of your vulnerability report within 48 hours. We will provide a timeline for a patch and will credit you in our Release Notes once the issue is securely resolved.
