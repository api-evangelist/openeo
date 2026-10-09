---
name: openeo-batch-job
description: Create, estimate, start, monitor and download the results of an openEO batch job.
api: openEO API
operations: [create-job, estimate-job, start-job, describe-job, debug-job, list-results, stop-job, delete-job]
---
# Run a batch job
1. `create-job` (POST /jobs) with the process graph; the job id is in the `OpenEO-Identifier` header.
2. Optionally `estimate-job` (GET /jobs/{job_id}/estimate) for cost/duration.
3. `start-job` (POST /jobs/{job_id}/results) to queue processing.
4. Poll `describe-job` (GET /jobs/{job_id}) until status is `finished` or `error`; read `debug-job` logs on error.
5. `list-results` (GET /jobs/{job_id}/results) returns STAC assets with download links.
6. `stop-job` cancels; `delete-job` removes the job. POST creation is not idempotent: check `list-jobs` before retrying a failed create.
