# `agent-fault-check` Pro Releases (`afc-pro`)

This repository distributes compiled, checksum-verified **`afc-pro`** release binaries for [`agent-fault-check`](https://github.com/evhu-dev/agent-fault-check).

- **Open-source core & documentation:** https://github.com/evhu-dev/agent-fault-check
- **Commercial license terms:** [COMMERCIAL_TERMS.md](COMMERCIAL_TERMS.md)
- **Pro features:** Unlimited scenarios, Redis & HTTP state assertion packs, SARIF 2.1.0 PR annotations, and JUnit XML reports (requires an active Polar license key via `AFC_LICENSE_KEY`).

## Usage in GitHub Actions

```yaml
- uses: evhu-dev/agent-fault-check@v0.1.0
  with:
    spec-path: "examples/checkout/chaos-spec.yaml"
    version: "v0.1.0"
    release-repository: "evhu-dev/agent-fault-check-releases"
    report-mode: "both" # console | junit | sarif | both
    license-key: ${{ secrets.AFC_LICENSE_KEY }}
```

## Security & Privacy
- Every release archive is verified against SHA-256 `checksums.txt`.
- No telemetry or phone-home analytics are collected; outbound calls are limited to Polar license validation (`api.polar.sh`).
