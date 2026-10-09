---
name: openeo-file-workspace
description: Upload, list, download and delete files in the user's openEO file workspace.
api: openEO API
operations: [list-files, upload-file, download-file, delete-file]
---
# File workspace
1. `upload-file` (PUT /files/{path}) with the raw body; PUT overwrites, so it is idempotent.
2. `list-files`, `download-file`, `delete-file` manage the stored files.
