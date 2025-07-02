# 🔍 SBOM Vulnerability Scan Report: Flask Project

**Date:** July 2, 2025  
**Toolchain:** Syft + Grype + jq
**Target:** [pallets/flask](https://github.com/pallets/flask)

---

## ✅ SBOM Summary

- Generated using `syft . -o cyclonedx-json > sbom.json`
- CycloneDX format (JSON)
- Key components detected:
  - Werkzeug 2.3.3
  - Jinja2 3.1.2

---

## 🚨 Vulnerability Findings (via Grype)

| Package   | Installed | Fixed In | Vulnerability ID      | Severity | Risk |
|-----------|-----------|----------|------------------------|----------|------|
| Werkzeug  | 2.3.3     | 3.0.6    | GHSA-q34m-jh98-gwm2    | Medium   | 0.8  |
| Werkzeug  | 2.3.3     | 2.3.8    | GHSA-hrfv-mqp8-q5rw    | Medium   | 0.2  |
| Werkzeug  | 2.3.3     | 3.0.3    | GHSA-2g68-c3qc-8985    | High     | 0.1  |
| Jinja2    | 3.1.2     | 3.1.6    | Multiple GHSA IDs      | Medium   | <0.1 |

---

<pre> ## 📊 Full Grype Scan Output ``` ✔ Vulnerability DB [updated] ✔ Scanned for vulnerabilities [9 vulnerability matches] ├── by severity: 0 critical, 1 high, 8 medium, 0 low, 0 negligible └── by status: 9 fixed, 0 not-fixed, 0 ignored NAME INSTALLED FIXED IN TYPE VULNERABILITY SEVERITY EPSS % RISK werkzeug 2.3.3 3.0.6 python GHSA-q34m-jh98-gwm2 Medium 78.67 0.8 werkzeug 2.3.3 2.3.8 python GHSA-hrfv-mqp8-q5rw Medium 60.59 0.2 werkzeug 2.3.3 3.0.3 python GHSA-2g68-c3qc-8985 High 37.42 0.1 jinja2 3.1.2 3.1.4 python GHSA-h75v-3vvj-5mfj Medium 41.56 < 0.1 jinja2 3.1.2 3.1.5 python GHSA-q2x7-8rv6-6q7h Medium 29.29 < 0.1 jinja2 3.1.2 3.1.3 python GHSA-h5c8-rqwp-cp95 Medium 27.34 < 0.1 jinja2 3.1.2 3.1.5 python GHSA-gmj6-6f8f-6699 Medium 20.39 < 0.1 werkzeug 2.3.3 3.0.6 python GHSA-f9vj-2wh5-fj8j Medium 10.85 < 0.1 jinja2 3.1.2 3.1.6 python GHSA-cpwx-vrp4-4pq7 Medium 8.40 < 0.1 ``` </pre>

---

## 🧠 Analysis

- **All vulnerabilities are patchable** with currently available versions.
- These vulnerabilities could expose Flask applications to code injection, denial-of-service, or data leakage.

---

## 🔧 Recommendations

- Upgrade to:
  - `werkzeug >= 3.0.6`
  - `jinja2 >= 3.1.6`
- Regenerate SBOM after upgrading and re-scan.
- Automate this scanning process in CI pipelines for future builds.

---
