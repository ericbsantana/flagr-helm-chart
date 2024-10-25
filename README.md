# Helm chart for Flagr

This is a Helm chart for [Flagr](https://github.com/openflagr/flagr), a feature flagging and configuration management platform.

## Installing the Chart

To install the chart with the release name `flagr`:

```bash
helm repo add flagr https://ericbsantana.github.io/flagr-helm-chart
```
```bash
helm install flagr flagr/flagr --devel # --devel is required for alpha versions
```

## Documentation

Reach the README at [charts/flagr/README.md](charts/flagr/README.md).
