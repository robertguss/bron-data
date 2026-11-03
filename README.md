# bron-data

The data of [Bron](https://github.com/robertguss/bron): texts, alignments, lexicon, provenance, and the rights registry. Code lives in the `bron` repo; this repo is the durable asset and is meant to outlive the software (Bron principle 1).

## Layout (CapiTainS conventions; see `bron/docs/text-model.md`)

```
data/                      TEI texts, one directory per textgroup, then per work
  bavinck/
    __cts__.xml
    gd/
      __cts__.xml
      bavinck.gd.ed1.xml        first edition (1895–1901)
      bavinck.gd.ed2.xml        second edition (1906–1911), base text of ed2
      bavinck.gd.ed2.bron-eng.xml   Bron's English of ed2
alignments/                stand-off TEI link files (ADR 0006)
lexicon/                   TBX termbase (ADR 0008)
provenance/                stand-off scores and flags (ADR 0009)
registry/                  works, source copies, rights statements (ADR 0012)
segmentation/              SRX rules
```

Only `alignments/` has content yet: the GD¹ ↔ GD² structural concordance.

## Licensing (two kinds of content, two licenses)

- **Transcriptions of public-domain works, metadata, and the registry** are not Bron's to license. They are marked with the Public Domain Mark where the underlying work is public domain, and any residual rights Bron might hold in them are waived under **CC0 1.0** (`LICENSE-CC0`). Bron claims no rights in Bavinck's, Kuyper's, Calvin's or Augustine's words.
- **Content authored by Bron and its contributors** — translations, lexicon definitions and rationales, alignment judgments and annotations, documentation — is licensed **CC BY 4.0** (`LICENSE`). Attribution is to "Bron contributors" and, where recorded, to the named reviewer; see `CITATION.cff`.

Each file states which applies in its TEI header or front matter.

## Contributing

Open a pull request. Corrections to texts and translations are welcome from anyone; the `reviewed` state can only be set by a vetted reviewer (see `REVIEWERS.md`, to be added with the first release, and ADR 0009 in the `bron` repo). CI will validate TEI, CapiTainS and DTS conformance and refuse changes that break a citation.

## Status

Design complete; no texts yet. See `bron/docs/roadmap.md`.
