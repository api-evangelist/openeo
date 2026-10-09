---
name: openeo-secondary-services
description: Publish a process graph as a secondary web service (e.g. XYZ tiles, WMTS) and manage it.
api: openEO API
operations: [list-service-types, create-service, describe-service, update-service, debug-service, delete-service, list-services]
---
# Secondary web services
1. `list-service-types` for supported protocols.
2. `create-service` (POST /services); the id is in `OpenEO-Identifier`.
3. `describe-service` for the access URL; `update-service` (PATCH) to change it; `debug-service` for logs; `delete-service` to remove.
