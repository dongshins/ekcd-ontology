# EKCD

EKCD is an EKC-derived ontology in OWL/Turtle designed to refine and extend selected areas of the EKC data model for more explicit, maintainable, and reusable knowledge modeling. Developed by Dong Shin SEO, it preserves conceptual continuity with EKC while supporting further specialization for Korean cultural heritage and digital humanities research.

**Repository:** `ekcd-ontology`  
**Ontology title:** `EKCD: EKC Derived Ontology`
**Namespace prefix:** `ekcd:`  
**Preferred namespace URI:** `http://dh.aks.ac.kr/ontologies/ekcd#`

---

## Overview

EKCD is a derivative ontology based on the previously released EKC ontology.  
It is designed to support ongoing personal extensions, especially in areas that were not formally incorporated into the institutional EKC release line.

Rather than replacing EKC, EKCD is intended as:

- a **derived ontology** that preserves conceptual continuity with EKC,
- a **working extension layer** for newly introduced properties and modeling decisions,
- a **practical ontology base** for building ABox and links datasets through Protégé and Cellfie.

---

## Relationship to EKC

EKCD is derived from EKC and is intended to remain interoperable with it.

In principle:

- **institutional EKC** remains the public institutional baseline,
- **EKCD** manages selected personal extensions and refinements by Dong Shin SEO,
- datasets built in the current workflow may use **EKCD as the active TBox** while still reusing the conceptual backbone of EKC.

EKCD therefore should be understood as a **derivative and extensible companion ontology**, not as a direct replacement for EKC.

---

## License

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
