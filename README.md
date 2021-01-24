# Cronjobs helm chart

With this helm chart you can create multiple cronjobs executing scripts.

## TL;DR

```bash
helm upgrade echo cronjobs --install
```

## Example with httpie

Cronjobs for executing http requests with httpie. Create `values.yaml`:

```yaml
schedulers:
- name: post-scheduler
  schedule:  "*/1 * * * *"
  script: |
    http -v POST https://httpbin.org/post
- name: get-scheduler
  schedule:  "*/2 * * * *"
  script: |
    http -v GET https://httpbin.org/get

image:
  repository: alpine/httpie
```

```bash
helm upgrade httpie cronjobs --install -f values.yaml
```

## Parameters

see [`values.yaml`](cronjobs/values.yaml)
