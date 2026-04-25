# Changelog

All notable changes to this project will be documented in this file.

This project follows:
- Semantic Versioning (SemVer) for public releases (e.g., `v1.0.4`)
- A release-documentation workflow based on versioned GitHub releases and archived ontology snapshots

## Evidence for ontology-header dates

- The primary date shown in a release header is based on the ontology-header values in the released TTL, especially `dcterms:issued` and `dcterms:modified`.
- If the GitHub publication date differs from the ontology-header date, the ontology-header date remains the primary documentary reference for ontology revision timing.

---

## EKCD v1.0.4 — 2026-04-17 (First Public Release)

### Overview

**EKCD v1.0.4** is the first public release of the **EKCD (EKC-derived) ontology** line.
It establishes an archived and citable baseline for a derivative ontology that extends EKC for ongoing Korean cultural heritage knowledge modeling, especially in areas of date-oriented datatype properties, operational mapping guidance, and project-level semantic extensions.

### Added

- First public release of the `ekcd:` ontology line
- Publicly versioned ontology metadata for **EKCD v1.0.4**
- Import relationship to **EKC 2025** as the institutional baseline
- Date-oriented datatype properties:
  - `ekcd:occurrenceDate`
  - `ekcd:startDate`
  - `ekcd:endDate`
  - `ekcd:originalDate`
  - `ekcd:accessURL`
- Local operational guidance for:
  - `owl:sameAs`
  - `skos:mappingRelation`
  - `skos:exactMatch`
  - `skos:closeMatch`
- Local usage notes for `edm:isShownAt` / `edm:isShownBy` with `ekcd:accessURL`

### Positioning

- **EKC** remains the institutional baseline ontology.
- **EKCD** is maintained as a derivative and extensible companion ontology.
- The current release should be read as an initial public archival baseline, not as a replacement of EKC.

### Compatibility

- The ontology imports **EKC 2025** and is intended to remain interoperable with the EKC conceptual backbone.
- Datasets may use EKCD as an active TBox in workflows that require derivative extensions.

### Documentation

- Release note: [`docs/releases/v1.0.4.md`](https://github.com/dongshins/ekcd-ontology/blob/main/docs/releases/v1.0.4.md)

### Links

- Release: [`v1.0.4`](https://github.com/dongshins/ekcd-ontology/releases/tag/v1.0.4)
- Compare: not applicable for the first public release
