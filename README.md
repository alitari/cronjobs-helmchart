# Cronjobs helm chart

With this helm chart you can create multiple cronjobs executing scripts.

## TL;DR

```bash
helm upgrade echo cronjobs --install
```

## Example with httpie

```bash
helm upgrade httpie cronjobs --install -f httpie-sample-values.yaml
```

## Parameters

see [`values.yaml`](cronjobs/values.yaml)
