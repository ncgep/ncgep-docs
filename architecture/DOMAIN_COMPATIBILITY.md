# Domain compatibility profile

Profile id: `ncgep.compat.v1`

Implemented in [`ncgep-domain-kit/compat`](https://github.com/ncgep/ncgep-domain-kit).

A compatible network publishes a manifest declaring:

- schema version;
- domain id / network id / chain id;
- environment;
- Bech32 prefixes;
- base denoms and optional asset descriptors with **origin** fields;
- security declaration (validator model, permissioned flag, …);
- classification (`official` | `compatible` | `experimental` | `private`);
- IBC capability flags (claims, not proofs);
- Domain Kit profile version.

Compatibility is technical/tooling metadata. It does **not** imply NCGEP endorsement
or equal trust with official networks.
