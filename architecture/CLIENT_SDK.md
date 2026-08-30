# Client SDK (TypeScript)

NCGEP’s first public client library is **`@ncgep/client`** in repository [`ncgep-client-ts`](https://github.com/ncgep/ncgep-client-ts).

## Layers

1. **Low-level** — CosmJS for standard Cosmos messages/queries; typed envelopes for `/ncgep.gaming.v1.*` and `/ncgep.enterprise.v1.*`; Domain REST for custom state.
2. **High-level NCGEP** — manifests (`ncgep.manifest.v1`), compatibility profile (`ncgep.compat.v1`), canonical asset origin (`ncgep://…`), explicit network contexts, Domain Bech32 rendering.

Clients must **not** infer chain identity from Bech32 strings or token symbols alone.

## Quickstart

```ts
import { NcgepClient, parseManifest, addressFromMnemonic } from "@ncgep/client";

const manifest = parseManifest(rawJson);
const client = NcgepClient.forNetwork(manifest, {
  rpc: "http://127.0.0.1:26657",
  api: "http://127.0.0.1:1317",
});
await client.connect();
```

Versioning is pre-1.0 (`0.1.0-dev`) and is **not** mirrored from Core/Gaming/Enterprise SemVer.

## Related products

- `ncgep-wallet` — PRIVATE multi-Domain signing UX prototype
- `ncgep-explorer` — PRIVATE multi-Domain read UX prototype

Both consume the same SDK; they must not reimplement protocol serialization.

## Limitations (current)

- IBC deferred — no transfer API
- Custom protobuf generation incomplete — REST + CosmJS bank for PHASE_10 demos
- Mnemonic helper is DEVELOPMENT only
- npm publication requires an explicit human gate after CI/readme/license checks
