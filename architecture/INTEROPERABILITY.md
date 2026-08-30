# Interoperability

IBC is the intended interoperability protocol between Core and Domains.

Current status: **implementation deferred** until an official IBC-Go release
compatible with NCGEP’s Cosmos SDK / CometBFT family is available. NCGEP will
not use unreleased pins, custom bridges, or fake Dalet mints on Domains.

When IBC is enabled:

- Domains remain sovereign if a counterparty or relayer fails;
- relayers provide liveness, not custody;
- technical connectivity ≠ official recognition;
- clients should map logical routes rather than hardcoding a single channel id.
