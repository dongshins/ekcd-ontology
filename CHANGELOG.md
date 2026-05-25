# Changelog

All notable changes to the EKCD ontology release line are documented in this file.

The format follows a practical Keep-a-Changelog style, and version numbers follow the GitHub/Zenodo release tags used for the ontology snapshots.

The project follows a conservative semantic-versioning practice for ontology releases. Patch releases may include metadata clarification, documentation improvement, local authoring-policy clarification, and non-breaking vocabulary declarations. Minor releases may include non-breaking vocabulary expansion.

## [v1.1.2] - 2026-05-25

**Zenodo DOI:** https://doi.org/10.5281/zenodo.20379676

### Added

- Added classes and properties for interpretive assertions, confidence levels, evidence tracking, and utterance modeling in historical knowledge graphs.
- Added EKCD-local classes for interpretive and utterance modeling:
  - `ekcd:InterpretiveAssertion`
  - `ekcd:InterpretiveConfidenceLevel`
  - `ekcd:Utterance`
  - `ekcd:RoyalUtterance`
  - `ekcd:RoyalCommand`
  - `ekcd:RetrospectiveUtterance`
- Added object properties for interpretive assertion modeling:
  - `ekcd:assertsSubject`
  - `ekcd:assertsPredicate`
  - `ekcd:assertsObject`
  - `ekcd:hasInterpretiveConfidence`
- Added object properties for correspondence and contextual association:
  - `ekcd:correspondsTo`
  - `ekcd:contextuallyRelatedTo`
- Added object properties for utterance modeling:
  - `ekcd:hasSpeaker`
  - `ekcd:isUtteranceRecordedIn`
  - `ekcd:utteranceAbout`
  - `ekcd:retrospectivelyFrames`
- Added datatype properties for evidence and utterance documentation:
  - `ekcd:evidenceLocation`
  - `ekcd:evidenceNote`
  - `ekcd:utteranceText`
- Added controlled confidence-level individuals:
  - `ekcd:Direct`
  - `ekcd:Probable`
  - `ekcd:Contextual`
- Added `dc:contributor` metadata for Su-jeong PARK / 박수정, including ORCID reference.

### Changed

- Updated `owl:versionInfo` from `EKCD v1.0.8` to `EKCD v1.1.2`.
- Updated `dcterms:modified` from `2026-05-08` to `2026-05-25`.
- Updated `owl:priorVersion` and `dcterms:replaces` to point to the preceding EKCD release file, `http://dh.aks.ac.kr/ontologies/ekcd_v1_0_8.ttl`.
- Expanded ontology-level descriptions to record the v1.1.x feature family for interpretive assertions, confidence levels, evidence tracking, and utterance modeling.

### Removed

- No v1.0.8 vocabulary term declarations were removed.
- Removed only the replaced ontology-version metadata values for `owl:versionInfo`, `dcterms:modified`, `owl:priorVersion`, and `dcterms:replaces`.

### Compatibility

- Existing v1.0.8 classes, object properties, EKCD-local datatype properties, and annotation properties remain compatible.
- Existing ABox data using v1.0.8 vocabulary terms should remain compatible with v1.1.2.
- v1.1.2 should be treated as a non-breaking vocabulary-expansion release.
- Recommended maintenance action: use the new interpretive-assertion, confidence-level, evidence-tracking, and utterance-modeling terms when modeling correspondence, contextual association, source evidence, and recorded utterances.

### Diff summary against v1.0.8

| Metric | v1.0.8 | v1.1.2 | Change |
|---|---:|---:|---:|
| RDF triples | 151 | 321 | +170 |
| Added triples | — | 174 | +174 |
| Removed triples | — | 4 | -4 |
| OWL classes | 3 | 11 | +8 |
| OWL object properties | 25 | 36 | +11 |
| OWL datatype properties | 5 | 8 | +3 |
| OWL annotation properties | 19 | 19 | 0 |
| OWL named individuals | 4 | 7 | +3 |
| SKOS concepts | 0 | 3 | +3 |

## [v1.0.8] - 2026-05-08

**Zenodo DOI:** https://doi.org/10.5281/zenodo.20078236

### Added

- Added `ekcd:authoringPolicy` as an OWL annotation property.
- Added bilingual labels and comments for `ekcd:authoringPolicy`.
- Added ontology-level `ekcd:authoringPolicy` statements in Korean and English.
- Added explicit OWL annotation property declarations for:
  - `vann:preferredNamespacePrefix`
  - `vann:preferredNamespaceUri`
- Added `owl:NamedIndividual` typing for the EKCD ontology resource, while preserving its `owl:Ontology` and `voaf:Vocabulary` roles.
- Added `rdfs:seeAlso <http://dh.aks.ac.kr/ontologies/ekc>` to connect EKCD directly to the canonical EKC ontology resource.

### Changed

- Updated `owl:versionInfo` from `EKCD v1.0.7` to `EKCD v1.0.8`.
- Updated `dcterms:modified` from `2026-05-07` to `2026-05-08`.
- Changed `dcterms:source` from the EKC GitHub repository URL to the canonical EKC ontology IRI:
  - from `https://github.com/dongshins/EKC_ontology`
  - to `http://dh.aks.ac.kr/ontologies/ekc`
- Revised the Korean ontology description to retain technical terms such as `datatype properties`, `properties`, and `semantic` for closer alignment with the ontology design vocabulary.
- Removed the Turtle `@base` declaration from the source serialization in line with the new authoring policy.

### Removed

- Removed the ontology-level English `rdfs:comment` that described the general EKC ontology history. The EKC relationship is now expressed through `dcterms:source` and `rdfs:seeAlso`.

### Compatibility

- No OWL classes were added or removed.
- No OWL object properties were added or removed.
- No EKCD-local datatype properties were added or removed.
- Existing ABox data using v1.0.7 vocabulary terms should remain compatible with v1.0.8.
- Recommended maintenance action: update Turtle authoring workflows to avoid `@base`, the empty prefix `:`, and relative IRIs.

### Diff summary against v1.0.7

| Metric | v1.0.7 | v1.0.8 | Change |
|---|---:|---:|---:|
| RDF triples | 141 | 151 | +10 |
| Added triples | — | 16 | +16 |
| Removed triples | — | 6 | -6 |
| OWL classes | 3 | 3 | 0 |
| OWL object properties | 25 | 25 | 0 |
| OWL datatype properties | 5 | 5 | 0 |
| OWL annotation properties | 16 | 19 | +3 |
| OWL named individuals | 3 | 4 | +1 |

## [v1.0.7] - 2026-05-07

### Baseline

- Previous released EKCD ontology version used as the comparison baseline for v1.0.8.
- Declared EKCD-local datatype properties for access URLs and date modeling.
- Included local guidance for `owl:sameAs`, `skos:exactMatch`, `skos:closeMatch`, and `skos:mappingRelation`.

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

[v1.1.2]: https://github.com/dongshins/ekcd-ontology/releases/tag/v1.1.2
[v1.1.2 DOI]: https://doi.org/10.5281/zenodo.20379676
[v1.0.8]: https://github.com/dongshins/ekcd-ontology/releases/tag/v1.0.8
[v1.0.8 DOI]: https://doi.org/10.5281/zenodo.20078236
[v1.0.7]: https://github.com/dongshins/ekcd-ontology/releases/tag/v1.0.7
[1.0.4]: https://github.com/dongshins/ekcd-ontology/releases/tag/v1.0.4
