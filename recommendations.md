# Recommendations for Fixing Vulnerabilities

Instead of downgrading @grafana/data and @grafana/runtime, which could introduce compatibility issues, we recommend the following changes to package.json:

1. Keep @grafana/data and @grafana/runtime at version 11.5.0-pre
2. Update dompurify to the latest version (3.0.5 or newer) to address the vulnerabilities

```json
{
  "version": "11.5.0-pre",
  "dependencies": {
    "@emotion/css": "11.13.5",
    "@grafana/data": "11.5.0-pre",
    "@grafana/runtime": "11.5.0-pre",
    "@grafana/schema": "11.5.0-pre",
    "@grafana/ui": "11.5.0-pre",
    "dompurify": "^3.0.5",
    "fast-deep-equal": "^3.1.3"
  }
}
```

This approach maintains compatibility with other Grafana packages while addressing the vulnerabilities in dompurify.
