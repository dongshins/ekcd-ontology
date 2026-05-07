# EKCD

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19753664.svg)](https://doi.org/10.5281/zenodo.19753664)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

**EKCD** is an EKC-derived ontology in OWL/Turtle for extensible Korean cultural heritage knowledge modeling. It refines selected areas of the EKC data model while preserving conceptual continuity with the EKC ontology line.

- **Repository:** `ekcd-ontology`
- **Ontology IRI:** `http://dh.aks.ac.kr/ontologies/ekcd`
- **Version IRI:** `http://dh.aks.ac.kr/ontologies/ekcd_v1`
- **Preferred namespace prefix:** `ekcd:`
- **Preferred namespace URI:** `http://dh.aks.ac.kr/ontologies/ekcd#`
- **Current release:** `v1.0.7`
- **Concept DOI, all versions:** `10.5281/zenodo.19753664`
- **License:** Creative Commons Attribution-ShareAlike 4.0 International (`CC-BY-SA-4.0`)

## Overview

EKCD is a derivative ontology based on the EKC ontology. It supports ongoing ontology refinement and dataset construction for Korean cultural heritage and digital humanities research, especially where project-level modeling decisions need to be maintained outside the institutional EKC release line.

EKCD is intended to serve as:

- a derived ontology that preserves conceptual continuity with EKC;
- a working extension layer for local or project-level modeling decisions;
- a practical TBox for producing ABox and links datasets through Protégé, spreadsheet templates, and Cellfie workflows;
- a citable repository release line for OWL/Turtle vocabulary maintenance.

## Relationship to EKC

EKCD does not replace EKC. It is a derivative and extensible companion ontology.

In this repository:

- institutional EKC remains the public baseline ontology line;
- EKCD manages selected extensions, refinements, and local usage guidance by Dong Shin SEO;
- datasets produced in the current workflow may use EKCD as the active TBox while remaining interoperable with the conceptual backbone of EKC.

The ontology imports `http://dh.aks.ac.kr/ontologies/ekc-2025` and records the EKC source repository as `https://github.com/dongshins/EKC_ontology`.

## Scope

The current EKCD release line covers three main areas.

### 1. Additional datatype properties

EKCD provides datatype properties used in date- and web-resource-oriented cultural heritage modeling:

- `ekcd:occurrenceDate`
- `ekcd:startDate`
- `ekcd:endDate`
- `ekcd:originalDate`
- `ekcd:accessURL`

### 2. Local usage guidance for standard mapping predicates

EKCD keeps standard semantic-web predicates while adding local operational guidance for EKCD modeling practice, including:

- `owl:sameAs`
- `skos:exactMatch`
- `skos:closeMatch`
- `skos:mappingRelation`
- `edm:isShownAt`
- `edm:isShownBy`

### 3. Repository-level ontology publication metadata

Since `v1.0.7`, the ontology record is also typed as `voaf:Vocabulary` and declares VANN namespace metadata:

- `vann:preferredNamespacePrefix "ekcd"`
- `vann:preferredNamespaceUri "http://dh.aks.ac.kr/ontologies/ekcd#"`

## Latest release: v1.0.7

`v1.0.7` is a metadata and namespace-clarification release based on comparison with `v1.0.4`.

Summary of ontology-level changes:

- added `voaf:Vocabulary` typing to the ontology resource;
- added VANN preferred namespace metadata;
- revised English and Korean ontology descriptions;
- revised ontology title metadata;
- updated `dcterms:modified` from `2026-04-17` to `2026-05-07`;
- updated `owl:versionInfo` from `EKCD v1.0.4` to `EKCD v1.0.7`;
- revised the Korean description of `ekcd:occurrenceDate` to use explicit `ekcd:` prefix references.

No classes, object properties, datatype properties, or annotation properties were added or removed between `v1.0.4` and `v1.0.7`.

For details, see [`docs/changes/v1.0.7-ontology-revision.md`](docs/changes/v1.0.7-ontology-revision.md).

## Repository structure

```text
ekcd-ontology/
├─ README.md
├─ CHANGELOG.md
├─ CITATION.cff
├─ .zenodo.json
├─ LICENSE
├─ vocab/
│  ├─ ekcd.ttl
│  └─ versions/
│     └─ ekcd_v1_0_7.ttl
└─ docs/
   └─ changes/
      └─ v1.0.7-ontology-revision.md
```

If the actual ontology file is stored under a different path, keep the DOI/citation metadata unchanged and adjust only the file-path references above.

## Data production workflow

EKCD is intended to support a practical ontology-driven workflow:

1. maintain the TBox in Protégé;
2. prepare researcher input in spreadsheet templates;
3. transform spreadsheet data into RDF/OWL through Cellfie;
4. generate an ABox dataset and a separate links dataset;
5. validate the outputs before public release;
6. publish citable ontology snapshots through GitHub Releases and Zenodo.

## Citation

For general citation of the EKCD ontology release line, use the Concept DOI:

> SEO, Dong Shin. **EKCD: An EKC-derived Ontology for Korean Cultural Heritage Knowledge Modeling**. Version 1.0.7. Zenodo, 2026. https://doi.org/10.5281/zenodo.19753664

For exact reproducibility, cite the Version DOI assigned by Zenodo to the specific release used. After the `v1.0.7` GitHub release is archived by Zenodo, replace or supplement the citation above with the Zenodo Version DOI for `v1.0.7`.

## Maintainer

**Dong Shin SEO**  
ORCID: <https://orcid.org/0009-0007-4477-6547>

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).
