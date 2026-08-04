# SCORM

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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

| Specification | API Object | Description |
|---------------|-----------|-------------|
| [SCORM 1.2](https://scorm.com/scorm-explained/technical-scorm/scorm-12-overview-for-developers/) | `API` | JavaScript API with 6 lesson status values (passed, failed, completed, incomplete, browsed, not attempted) and CMI data model |
| [SCORM 2004](https://scorm.com/scorm-explained/technical-scorm/scorm-2004-overview-for-developers/) | `API_1484_11` | Extended API with separate completion and success status, scaled scores, and IMS Simple Sequencing |
| [xAPI / Tin Can](https://xapi.com/) | LRS | Modern successor using a Learning Record Store (LRS) and statement-based tracking (subject-verb-object) |

## SCORM API Functions

### SCORM 1.2 Functions
| Function | Description |
|----------|-------------|
| `LMSInitialize("")` | Initialize the SCORM session |
| `LMSGetValue(element)` | Read a CMI data model value |
| `LMSSetValue(element, value)` | Write a CMI data model value |
| `LMSCommit("")` | Persist data to the LMS |
| `LMSFinish("")` | End the SCORM session |
| `LMSGetLastError()` | Get the last error code |
| `LMSGetErrorString(code)` | Get a human-readable error message |
| `LMSGetDiagnostic(code)` | Get diagnostic detail for an error |

### SCORM 2004 Functions (equivalent)
| Function | Description |
|----------|-------------|
| `Initialize("")` | Initialize the session |
| `GetValue(element)` | Read a CMI data model value |
| `SetValue(element, value)` | Write a CMI data model value |
| `Commit("")` | Persist data |
| `Terminate("")` | End the session |
| `GetLastError()` | Get last error code |
| `GetErrorString(code)` | Get error message |
| `GetDiagnostic(code)` | Get error diagnostic |

## Artifacts

### JSON Schema

| File | Description |
|------|-------------|
| [json-schema/scorm-cmi-data-schema.json](json-schema/scorm-cmi-data-schema.json) | SCORM CMI data model schema covering SCORM 1.2 and SCORM 2004 fields |

### JSON Structure

| File | Description |
|------|-------------|
| [json-structure/scorm-package-structure.json](json-structure/scorm-package-structure.json) | SCORM Package Interchange Format (PIF) structure and manifest |

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
- **ADL GitHub:** https://github.com/adlnet

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
