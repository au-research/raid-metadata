Guidelines for naming blocks and fields in the metadata schema documentation,
and how those names map to the actual RAiD API/data model implementation
(the LinkML model in `au-research/raid-au`, `api-svc/datamodel/src/v2/`).

**Note (2026-07-29):** this document previously described a flattened,
block-name-prefixed field convention (e.g. `identifierSchemeUri`,
`titleStartDate`). That convention was never actually implemented — neither
in the real API nor in this repository's own schema documentation, both of
which use the nested dot-path structure described below. This document has
been rewritten to describe what is actually implemented.

# Terminology

* Case name terms come from:
  https://web.archive.org/web/20230208161922/https://en.wikipedia.org/wiki/Naming_convention_(programming)#Examples_of_multiple-word_identifier_formats
  * examples:
    * "camel case": `identifier`
    * "pascal case": `Identifier`
* "Schema documentation" refers to the RST source in `rtd/docs/source/`
  (rendered at https://metadata.raid.org), which is itself sourced from the
  LinkML data model in `au-research/raid-au`.

# Block names

Block names aren't physically present in the metadata as a key, but they
name the LinkML class that defines a block's properties (e.g. the
`identifier` root field's values are defined by the LinkML class `Id`; the
`title` root field's values are defined by the class `Title`).

### Pluralisation

Always use the singular.

#### Examples

* use `Date`, not `Dates`
* use `Title`, not `Titles`

### Capitalisation

Pascal case, matching the LinkML class name directly — **no suffix** (e.g.
`Title`, `Access`, `Contributor`, `RelatedRaid`; not `TitleBlock`,
`AccessBlock`, etc.). Initialisms and acronyms are treated as proper words.

Schema documentation prose may use whatever reader-friendly capitalisation
makes sense (e.g. "identifierURL", "RAiD") — this never drives the actual
class/type name in the data model or API.

# Root fields

Fields at the root level of the metadata document that hold a block's
values.

### Naming standard

Use the same name as the block, camel case, singular.

#### Examples

* `identifier`
* `title`
* `relatedRaid` (not `relatedRAiDs`)
* `alternateUrl`

# Fields within a block (and sub-blocks)

Fields nested inside a block, or inside a sub-block nested within a block.

### Naming standard

Plain camel case, with **no** repetition of the parent block's name — the
nesting itself (dot-path) is what scopes the field, not a name prefix.

#### Examples

* `identifier` block (LinkML class `Id`):
  * `identifier.schemaUri`
  * `identifier.registrationAgency.id`
  * `identifier.registrationAgency.schemaUri`
  * `identifier.owner.id`
  * `identifier.owner.schemaUri`
  * `identifier.owner.servicePoint`
* `title` block (LinkML class `Title`):
  * `title.text`
  * `title.startDate`
  * `title.type.id`
  * `title.type.schemaUri`
* `relatedRaid` block (LinkML class `RelatedRaid`):
  * `relatedRaid.id`
  * `relatedRaid.type.id`
  * `relatedRaid.type.schemaUri`

This matches both the LinkML attribute names directly and the section
numbering already used throughout `rtd/docs/source/` (e.g.
`core/identifier.rst`'s `1.3.1 identifier.registrationAgency.id`).

---

# Worked example

```json
{
  "identifier": {
    "id": "https://raid.org/prefix/suffix",
    "schemaUri": "https://raid.org/",
    "registrationAgency": {
      "id": "https://ror.org/038sjwq14",
      "schemaUri": "https://ror.org"
    },
    "owner": {
      "id": "https://ror.org/038sjwq14",
      "schemaUri": "https://ror.org/",
      "servicePoint": 20000000
    },
    "license": "Creative Commons CC-0",
    "version": 1
  },
  "date": {
    "startDate": "2023-03-08"
  },
  "title": [
    {
      "text": "sto mint 1",
      "type": {
        "id": "https://vocabulary.raid.org/title.type.id/380",
        "schemaUri": "https://vocabulary.raid.org/title.type.schema/376"
      },
      "startDate": "2023-03-08"
    }
  ],
  "contributor": [
    {
      "id": "https://orcid.org/0009-0004-9651-5072",
      "schemaUri": "https://orcid.org/",
      "position": [
        {
          "id": "https://vocabulary.raid.org/contributor.position.schema/307",
          "schemaUri": "https://vocabulary.raid.org/contributor.position.schema/305",
          "startDate": "2023-03-08"
        }
      ],
      "role": [
        {
          "id": "https://credit.niso.org/contributor-roles/project-administration/",
          "schemaUri": "https://credit.niso.org/"
        }
      ]
    }
  ],
  "relatedRaid": [
    {
      "id": "https://raid.org/prefix/suffix",
      "type": {
        "id": "https://vocabulary.raid.org/relatedRaid.type.schema/204",
        "schemaUri": "https://vocabulary.raid.org/relatedRaid.type.schemaUri/285"
      }
    }
  ]
}
```
