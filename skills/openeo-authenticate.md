---
name: openeo-authenticate
description: Obtain a Bearer token for an openEO back-end via OpenID Connect or HTTP Basic and confirm the account.
api: openEO API
operations: [authenticate-oidc, authenticate-basic, describe-account]
---
# Authenticate
1. `authenticate-oidc` (GET /credentials/oidc) lists OIDC providers; authenticate with the provider and send `Authorization: Bearer oidc/{provider_id}/{access_token}`.
2. Or `authenticate-basic` (GET /credentials/basic) with HTTP Basic to receive an access token, then send `Authorization: Bearer basic//{token}`.
3. `describe-account` (GET /me) to confirm identity, storage and budget.
