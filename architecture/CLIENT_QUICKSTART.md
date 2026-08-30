# Developer Quickstart — Clients

1. Read [Network Manifests](./NETWORK_MANIFESTS.md) and [Asset Origin](./ASSET_ORIGIN.md).
2. Install `@ncgep/client` (when published) or clone `ncgep-client-ts`.
3. Load a validated manifest; create `NcgepClient.forNetwork` with an explicit RPC.
4. Derive Domain addresses from one key with Domain HRPs (`ncgep`, `ngame`, `nent`).
5. Treat symbols as display metadata — compare canonical origin tuples.

Do not deploy wallet/explorer prototypes publicly. Do not assume IBC exists.
