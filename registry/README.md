# registry

Where every text Bron shows came from, and why Bron may show it (Bron ADR 0012, amended by ADR 0017).

| File | Holds | Schema |
|---|---|---|
| `sources.yaml` | One record per work per source copy: holder, the holder's identifier, edition and printing, the work's rights status, URL, SHA-256, and mirrors | `bron/src/bron/schemas/registry-sources.schema.json` |
| `terms.yaml` | The terms of use of each site Bron takes copies from, with the date checked and a summary of the terms as they read | `bron/src/bron/schemas/registry-terms.schema.json` |

Three things are recorded apart:

- **A work's copyright status** is the `rights` field of a source record. It is a rightsstatements.org statement URI, or the Creative Commons Public Domain Mark or CC0 URI.
- **A site's access and reuse terms**, including database rights and bulk-download conditions, are a record in `terms.yaml`.
- **The status of Bron's own outputs** is stated in each output file's header (ADR 0014).

A terms record stays `pending` until Robert confirms it, which adds `confirmed_by` and `confirmed_on`. `bron check` validates both files on every pull request.

The registry is metadata, so it carries no license claim: any residual rights are waived under CC0 1.0 (`../LICENSE-CC0`).
