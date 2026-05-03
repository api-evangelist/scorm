# SCORM

SCORM (Sharable Content Object Reference Model) is a set of technical standards for e-learning software products. Originally developed by the Advanced Distributed Learning (ADL) Initiative under the U.S. Department of Defense, SCORM defines how online learning content and Learning Management Systems (LMS) communicate, enabling interoperability between authoring tools, content packages, and LMS platforms. Key versions include SCORM 1.2 and SCORM 2004, with xAPI (Tin Can) as the modern successor.

**Specification Site:** https://scorm.com/
**ADL Initiative:** https://adlnet.gov/projects/scorm/
**APIs.yml:** https://raw.githubusercontent.com/api-evangelist/scorm/refs/heads/main/apis.yml

## Scope

- **Type:** Standard
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- E-Learning
- LMS
- Standards
- Education
- Interoperability

## Specifications

| Specification | Description |
|---------------|-------------|
| [SCORM 1.2](https://scorm.com/scorm-explained/technical-scorm/scorm-12-overview-for-developers/) | JavaScript API (named "API"), 6 lesson status values, CMI data model |
| [SCORM 2004](https://scorm.com/scorm-explained/technical-scorm/scorm-2004-overview-for-developers/) | JavaScript API (named "API_1484_11"), separate completion/success status, IMS Sequencing |
| [xAPI / Tin Can](https://xapi.com/) | Modern successor using LRS, statement-based tracking |

## Artifacts

### JSON Schema

| File | Description |
|------|-------------|
| [json-schema/scorm-cmi-data-schema.json](json-schema/scorm-cmi-data-schema.json) | SCORM CMI data model schema |

### JSON Structure

| File | Description |
|------|-------------|
| [json-structure/scorm-package-structure.json](json-structure/scorm-package-structure.json) | SCORM Package Interchange Format (PIF) structure |

### JSON-LD

| File | Description |
|------|-------------|
| [json-ld/scorm-context.jsonld](json-ld/scorm-context.jsonld) | JSON-LD context for SCORM vocabulary |

### Examples

| File | Description |
|------|-------------|
| [examples/scorm-api-initialize-example.json](examples/scorm-api-initialize-example.json) | SCORM 1.2 API initialization and data exchange sequence |

### Vocabulary

| File | Description |
|------|-------------|
| [vocabulary/scorm-vocabulary.yml](vocabulary/scorm-vocabulary.yml) | SCORM normative vocabulary and e-learning taxonomy |

## Links

- **ADL SCORM Resources:** https://adlnet.gov/projects/scorm/
- **SCORM.com Technical Overview:** https://scorm.com/scorm-explained/technical-scorm/
- **Rustici Software (SCORM Authority):** https://rusticisoftware.com/scorm/
- **xAPI Specification (GitHub):** https://github.com/adlnet/xAPI-Spec

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
