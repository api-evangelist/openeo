---
name: openeo-discover-backend
description: Connect to an openEO back-end and discover its versions, capabilities, collections, processes and file formats.
api: openEO API
operations: [connect, capabilities, conformance, list-collections, describe-collection, list-collection-queryables, list-processes, list-file-types]
---
# Discover an openEO back-end
1. `connect` (GET /.well-known/openeo) on the back-end root to choose an API version and its base URL.
2. `capabilities` (GET /) to read the supported endpoints, billing and links. `conformance` lists conformance classes.
3. `list-collections` then `describe-collection` (STAC metadata) for the datasets you need; `list-collection-queryables` for filterable properties.
4. `list-processes` for the predefined processes and `list-file-types` for input/output formats.
All of these are read-only GET calls; many back-ends allow them without authentication.
