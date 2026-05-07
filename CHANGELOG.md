# Changelog

All notable changes to the EKCD ontology release line are documented in this file.

The format follows a practical Keep-a-Changelog style, and version numbers follow the GitHub/Zenodo release tags used for the ontology snapshots.

## [1.0.7] - 2026-05-07

### Added

- Added `voaf:Vocabulary` typing to the ontology resource `http://dh.aks.ac.kr/ontologies/ekcd`.
- Added VANN namespace metadata:
  - `vann:preferredNamespacePrefix "ekcd"`
  - `vann:preferredNamespaceUri "http://dh.aks.ac.kr/ontologies/ekcd#"`
- Added the `vann:` prefix declaration to the Turtle serialization.

### Changed

- Updated `owl:versionInfo` from `EKCD v1.0.4` to `EKCD v1.0.7`.
- Updated `dcterms:modified` from `2026-04-17` to `2026-05-07`.
- Revised ontology-level English and Korean descriptions to emphasize:
  - Korean cultural heritage knowledge modeling;
  - date and URL datatype-property support;
  - local application guidelines for standard semantic mapping predicates;
  - project-level semantic extensions.
- Revised ontology title metadata:
  - English: `EKCD: An EKC-derived Ontology for Korean Cultural Heritage Knowledge Modeling`
  - Korean: `EKCD: 한국 문화유산 지식 모델링을 위한 EKC 파생 온톨로지`

### Fixed

- Revised the Korean description of `ekcd:occurrenceDate` so that references to `startDate`, `endDate`, and `originalDate` use explicit `ekcd:` prefix notation instead of the local colon prefix.
- Removed the unused bare `:` prefix declaration from the Turtle header.

### Compatibility

- No classes were added or removed.
- No object properties were added or removed.
- No datatype properties were added or removed.
- No annotation properties were added or removed.
- Existing EKCD term IRIs remain stable.

### Ontology diff summary

| Metric | v1.0.4 | v1.0.7 | Change |
|---|---:|---:|---:|
| RDF triples | 138 | 141 | +3 net |
| OWL classes | 3 | 3 | 0 |
| OWL object properties | 25 | 25 | 0 |
| OWL datatype properties | 5 | 5 | 0 |
| OWL annotation properties | 16 | 16 | 0 |
| OWL ontology resources | 1 | 1 | 0 |

Triple-level comparison: 10 triples added and 7 triples removed.

## [1.0.4] - 2026-04-17

### Added

- First public DOI-backed EKCD ontology release.
- Published EKCD as an EKC-derived OWL/Turtle ontology for Korean cultural heritage and digital humanities modeling.
- Included initial EKCD datatype-property set:
  - `ekcd:occurrenceDate`
  - `ekcd:startDate`
  - `ekcd:endDate`
  - `ekcd:originalDate`
  - `ekcd:accessURL`
- Included local usage guidance for selected standard mapping and web-resource predicates, including `owl:sameAs`, `skos:exactMatch`, `skos:closeMatch`, `skos:mappingRelation`, `edm:isShownAt`, and `edm:isShownBy`.

[1.0.7]: https://github.com/dongshins/ekcd-ontology/releases/tag/v1.0.7
[1.0.4]: https://github.com/dongshins/ekcd-ontology/releases/tag/v1.0.4
