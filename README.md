# EKCD Ontology

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19753664.svg)](https://doi.org/10.5281/zenodo.19753664)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

**EKCD** is an EKC-derived ontology for Korean cultural heritage knowledge modeling. It extends the EKC ontology line with project-level modeling conventions, date- and URL-related datatype properties, and local guidance for semantic mapping properties.

- Current release: **v1.0.8**
- Ontology IRI: `http://dh.aks.ac.kr/ontologies/ekcd`
- Version IRI: `http://dh.aks.ac.kr/ontologies/ekcd_v1`
- Preferred prefix: `ekcd`
- Preferred namespace URI: `http://dh.aks.ac.kr/ontologies/ekcd#`
- Imported ontology: `http://dh.aks.ac.kr/ontologies/ekc-2025`
- Source ontology: `http://dh.aks.ac.kr/ontologies/ekc`
- License: [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/)

## Overview

EKCD supports RDF/OWL modeling for Korean cultural heritage data derived from, or aligned with, the EKC ontology family. The ontology is intentionally small and conservative: v1.0.8 preserves the v1.0.7 class, object property, and datatype property sets while clarifying ontology metadata and serialization policy.

The ontology currently includes:

| Category | Count in v1.0.8 | Notes |
|---|---:|---|
| OWL classes | 3 | Includes `ekc:3D_모델`, `ekc:3D_지도`, and `voaf:Vocabulary` declarations. |
| OWL object properties | 25 | Reuses selected DCMI Terms, EDM, FOAF, OWL, and SKOS properties for EKCD modeling. |
| OWL datatype properties | 5 | Adds EKCD-local properties for access URLs and date modeling. |
| OWL annotation properties | 19 | Adds explicit declarations for EKCD and VANN annotation properties. |
| OWL named individuals | 4 | Includes EKC/EKCD ontology resources and the DH-AKS organization resource. |

## Namespace policy

As of **v1.0.8**, EKCD declares an explicit authoring policy:

> EKCD TBox files and related ABox data do not use `@base` declarations, the empty prefix `:`, or relative IRIs such as `<#...>`, `<...>`, and `<>`. EKC and EKCD resources must be explicitly written with the `ekc:` or `ekcd:` prefixed names.

This policy is intended to make Turtle files easier to review, compare, and maintain across ontology and data releases.

Recommended prefixes:

```turtle
@prefix ekc:   <http://dh.aks.ac.kr/ontologies/ekc#> .
@prefix ekcd:  <http://dh.aks.ac.kr/ontologies/ekcd#> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix dc:    <http://purl.org/dc/elements/1.1/> .
@prefix edm:   <http://www.europeana.eu/schemas/edm/> .
@prefix foaf:  <http://xmlns.com/foaf/0.1/> .
@prefix owl:   <http://www.w3.org/2002/07/owl#> .
@prefix rdf:   <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:  <http://www.w3.org/2000/01/rdf-schema#> .
@prefix skos:  <http://www.w3.org/2004/02/skos/core#> .
@prefix xsd:   <http://www.w3.org/2001/XMLSchema#> .
```

## EKCD-local datatype properties

| Property | Range | Intended use |
|---|---|---|
| `ekcd:accessURL` | `xsd:anyURI` | Dereferenceable web address of a `WebResource` or `Multimedia` individual. In EKCD local practice, `edm:isShownBy` and `edm:isShownAt` remain object properties, while concrete URLs are recorded on the target resource with `ekcd:accessURL`. |
| `ekcd:occurrenceDate` | `xsd:date` | Normalized date of a single event, activity, or historical occurrence. |
| `ekcd:startDate` | `xsd:date` | Normalized start date of a period event. |
| `ekcd:endDate` | `xsd:date` | Normalized end date of a period event. |
| `ekcd:originalDate` | `rdfs:Literal` | Original date expression as attested in source materials, such as lunar-calendar or historically phrased dates. |

## Date modeling

Use `ekcd:occurrenceDate` for a single known occurrence date. For period events, prefer `ekcd:startDate` and `ekcd:endDate`. When the original source preserves a non-normalized date expression, record it with `ekcd:originalDate` as well.

Example:

```turtle
ekcd:SomeHistoricalEvent
    ekcd:startDate "1795-03-29"^^xsd:date ;
    ekcd:endDate "1795-04-05"^^xsd:date ;
    ekcd:originalDate "음력 1795년 윤2월 9일~16일"@ko .
```

## URL modeling

In EKCD local practice, keep Europeana display properties as object properties:

```turtle
ekcd:SomeObject
    edm:isShownAt ekcd:SomeLandingPage ;
    edm:isShownBy ekcd:SomeImageResource .

ekcd:SomeLandingPage
    ekcd:accessURL "https://example.org/page"^^xsd:anyURI .

ekcd:SomeImageResource
    ekcd:accessURL "https://example.org/image.jpg"^^xsd:anyURI .
```

## Semantic mapping guidance

EKCD distinguishes strict identity from conceptual or vocabulary mapping:

| Property | EKCD usage |
|---|---|
| `owl:sameAs` | Use only when two URIs denote the same individual/resource. Do not use for mere similarity, cross-reference, or concept mapping. |
| `skos:exactMatch` | Use for precise mapping between concepts in different concept schemes. It is not identical to OWL-level identity. |
| `skos:closeMatch` | Use for close but not fully identical concept mapping. |
| `skos:mappingRelation` | Super-property for mapping relations between different concept schemes. |

## Release history

See [`CHANGELOG.md`](CHANGELOG.md) for version history and [`docs/changes/v1.0.8-ontology-revision.md`](docs/changes/v1.0.8-ontology-revision.md) for the detailed v1.0.8 ontology revision note.

## Citation

If you use EKCD v1.0.8, please cite the version-specific Zenodo record: 

(EKCD v1.0.8을 사용한 연구에서는 재현성을 위해 다음의 version-specific DOI를 인용해 주세요. @ko)

> SEO, Dong Shin. (2026). *EKCD: An EKC-derived Ontology for Korean Cultural Heritage Knowledge Modeling* (v1.0.8). Zenodo. https://doi.org/10.5281/zenodo.20078236

For citing the EKCD ontology as an evolving project across versions, use the concept DOI:

(EKCD 온톨로지 전체 버전 계열을 포괄적으로 가리킬 때는 다음 concept DOI를 사용할 수 있습니다. @ko)

> https://doi.org/10.5281/zenodo.19753664

## Credits

EKCD was created by Dong Shin SEO as an EKC-derived ontology for Korean cultural heritage knowledge modeling. Su-jeong PARK contributed to the improvement of EKCD.

EKCD imports and derives from the EKC ontology line. The EKC Vocabulary Contributor Group is therefore acknowledged here as the contributor group for the source/imported EKC vocabulary, not as a statement that all members of the group directly contributed to EKCD. Among members of the EKC Vocabulary Contributor Group, direct EKCD work has been carried out by Dong Shin SEO and Su-jeong PARK.

- **EKCD creator**
  - Dong Shin SEO / 서동신

- **EKCD contributor**
  - Su-jeong PARK / 박수정

- **Source/imported ontology credit**
  - EKC Vocabulary Contributor Group

## Maintainer

- Dong Shin SEO / 서동신
- ORCID: `0009-0007-4477-6547`
- Contact point: `https://github.com/dongshins`
