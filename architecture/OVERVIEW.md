# NCGEP architecture overview

NCGEP is a multi-network Cosmos ecosystem:

- **Core** — sovereign Cosmos SDK chain; intended canonical origin of **Dalet**.
- **Domains** — sovereign Cosmos SDK networks (not L2s by default) for specialized
  workloads such as Gaming and Enterprise.
- **Domain Kit** — public Go library for shared conventions (Bech32 helpers,
  manifests, compatibility profile, asset-origin references).

Domains have independent genesis, state, validator sets, upgrades, and
security policy. Interoperability is intended via **IBC** when a compatible
released IBC-Go pin exists. Until then, Domains operate independently without
cross-chain asset movement.

There is **no** Cosmos Hub ICS / shared security requirement in the current
architecture.
