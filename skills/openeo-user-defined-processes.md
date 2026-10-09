---
name: openeo-user-defined-processes
description: Store, list, inspect and delete user-defined processes (process graphs) on an openEO back-end.
api: openEO API
operations: [store-custom-process, list-custom-processes, describe-custom-process, delete-custom-process, validate-custom-process]
---
# User-defined processes
1. `validate-custom-process` the graph first.
2. `store-custom-process` (PUT /process_graphs/{process_graph_id}) creates or replaces it; PUT is idempotent.
3. `list-custom-processes` and `describe-custom-process` to read them; `delete-custom-process` to remove.
