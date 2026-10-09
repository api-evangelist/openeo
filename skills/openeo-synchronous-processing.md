---
name: openeo-synchronous-processing
description: Validate a process graph and compute its result synchronously, downloading the output directly.
api: openEO API
operations: [validate-custom-process, compute-result]
---
# Synchronous processing
1. Build a process graph from processes returned by `list-processes`.
2. `validate-custom-process` (POST /validation) and fix any reported errors.
3. `compute-result` (POST /result) returns the data in the response body. Use it for small areas; large jobs should use batch jobs.
Errors follow the openEO error object (`code`, `message`, optional `id`, `links`).
