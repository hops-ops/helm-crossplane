# helm-crossplane

A Crossplane Configuration package that installs the Crossplane Helm chart with a minimal, stable interface.

## Overview

`helm-crossplane` renders a single Helm release for Crossplane. It exposes only the inputs needed
for chart values, namespace, and release name, keeping the interface stable while allowing full Helm overrides.

## Features

- **Minimal Helm interface**: values and overrideAllValues with stable defaults
- **Predictable naming**: defaults to `<clusterName>` in the `crossplane-system` namespace
- **GitOps friendly**: ships a `.gitops/` deploy chart

## Prerequisites

- Crossplane installed in the cluster
- Crossplane providers:
  - `provider-helm` (>=v1.0.2)
- Crossplane function:
  - `function-auto-ready` (>=v0.6.0)

## Quick Start

```yaml
apiVersion: pkg.crossplane.io/v1
kind: Configuration
metadata:
  name: helm-crossplane
spec:
  package: ghcr.io/hops-ops/helm-crossplane:latest
```

```yaml
apiVersion: helm.hops.ops.com.ai/v1alpha1
kind: Crossplane
metadata:
  name: crossplane
  namespace: example-env
spec:
  clusterName: example-cluster
  values:
    args:
      - --enable-composition-functions
```

## Development

```bash
make render
make validate
make test
```
