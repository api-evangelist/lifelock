# LifeLock

LifeLock is a consumer identity-theft-protection brand founded in 2005 in Tempe, Arizona and owned by Gen Digital, Inc. (Nasdaq: GEN). It monitors members' personal information for misuse, alerts them through its proprietary Identity Alert System, and provides U.S.-based restoration specialists plus reimbursement coverage when identity theft occurs.

**No public developer API.** LifeLock is a direct-to-consumer subscription service. Enrichment found no developer portal, OpenAPI, SDKs, MCP server, or `/.well-known/` discovery surface — `developer.lifelock.com`, `api.lifelock.com`, and `developer.gendigital.com` do not resolve. Spec-dependent artifacts are correctly absent rather than fabricated.

## What was found

- **`llms/lifelock-llms.txt`** — a real first-party `llms.txt` served at `https://lifelock.norton.com/llms.txt`, saved verbatim. This is LifeLock's machine-readable surface: plans, features, blog taxonomy, and explicit "Notes for AI Assistants" brand-disambiguation guidance.
- **`security/lifelock-vulnerability-disclosure.yml`** — disclosure is handled by parent Gen Digital via a central intake form covering all its brands.
- **`security/lifelock-domain-security.yml`** — TLS 1.3, HSTS, SPF and DMARC (`p=reject`) present; no DNSSEC, no CAA.
- **`well-known/lifelock-well-known.yml`** — honest negative record; every probed `/.well-known/` path returned 404.

Backed by: bessemer-venture-partners, ivp, kleiner-perkins — https://lifelock.norton.com/
