# Network manifests

Machine-readable network metadata lives in Domain Kit package `manifest`
(schema `ncgep.manifest.v1`).

Manifests support discovery for wallets/explorers. Integrity starts with
canonical checksums; repository or organizational signatures may be added later.

**Trust rule:** a file that claims to be NCGEP is not automatically trusted.
Official clients should pin known manifests / checksums from published sources.
