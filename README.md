# NCGEP Documentation

Public architecture and developer-facing documentation for the NCGEP ecosystem.

This repository does **not** contain internal control-plane records, private
network topology, or secrets. Those remain in private repositories.

## Contents

- [Architecture overview](architecture/OVERVIEW.md)
- [Core vs Domains](architecture/CORE_AND_DOMAINS.md)
- [Domain compatibility](architecture/DOMAIN_COMPATIBILITY.md)
- [Network manifests](architecture/NETWORK_MANIFESTS.md)
- [Asset origin](architecture/ASSET_ORIGIN.md)
- [Interoperability](architecture/INTEROPERABILITY.md)
- [Trust concepts](architecture/TRUST.md)
- [Client SDK](architecture/CLIENT_SDK.md)
- [Client quickstart](architecture/CLIENT_QUICKSTART.md)
- [Privacy Domain (R&D)](architecture/PRIVACY_RD.md)

## Related repositories

| Repo | Role | Visibility |
|---|---|---|
| `ncgep-domain-kit` | Domain conventions, manifests, compatibility | PUBLIC |
| `ncgep-client-ts` | TypeScript client SDK (`@ncgep/client`) | PUBLIC |
| `ncgep-core` | Core chain | PRIVATE (publication TBD) |
| `ncgep-gaming` | Gaming Domain | PRIVATE (publication TBD) |
| `ncgep-enterprise` | Enterprise Domain | PRIVATE (publication TBD) |
| `ncgep-wallet` / `ncgep-explorer` | Product prototypes | PRIVATE |

License: Apache-2.0 for documentation text unless otherwise noted.
