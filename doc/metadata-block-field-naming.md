Some guidelines for naming blocks and fields in the metadata schema 
documentation and how to implement the schema in the API implementation.


# Terminology

* Case name terms come from: 
https://web.archive.org/web/20230208161922/https://en.wikipedia.org/wiki/Naming_convention_(programming)#Examples_of_multiple-word_identifier_formats
  * examples:
    * "camel case" : "identifierBlock"  
    * "pascal case" : "IdentifierBlock"  
* "Schema documentation" refers to the Google drive
  [RAiD Metadata Schema v0-5](https://docs.google.com/document/d/1qL1evcBDv4KsV18wqm99RPg3iUNvVndZ1zKJY2i649Y/edit#)


# Schema documentation 

## Block names

Block names aren't physically present in the metadata, but their naming is used
to drive the API for things like field names - so we need to be careful and 
consistent.

### Pluralisation

Always use the singular.  Mostly just because english has weird and 
inconsistent pluralisation rules.

#### Examples

* use `Date`, not `Dates`
* use `Title`, not `Titles`

### Capitalisation

The schema documentation may use whatever case it wants, but it does not 
drive the capitalisation of field identifiers or type names in the API 
(defined below).

This allows the schema documentation to represent names in reader-friendly 
capitalisation that makes things easier for humans to understand, for example:
"identifierURL", or "RAiD". 

## Root fields

Talking here about fields at the root level of the meta schema, the fields that
contain the blocks.

### Naming standard

Use the same name as the block name.


## Block fields

Talking here about fields inside a block.

### Naming standard

Prepend the block name to the field name.

Yes, this means there's a lot of duplication of the block name withing the 
field names.

We don't know why we do this - we're just copying what DataCite and other 
schema definitions do.  It has the advantage of not needing any kind of 
exemptions or edge case rules (for example what do you do with `title.title`
if you insist on de-duplicating the names).

#### Examples

* `Identifier` block field names
  * `identifierSchemeURI`
  * `identifierServicePoint`
* `Date` block field names
  * `dateStart`
  * `dateEnd`

### Capitalisation

The schema documentation may use whatever case it wants, but it does not
drive the capitalisation of field identifiers or type names in the API
(defined below).

---

# API implementation 

## Block Type names

The "Type name" is a technical thing, in OpenAPI we map a metadata schema block 
as a [component schema](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.0.3.md#components-object).

In Java or TypeScript, the block maps to a class or interface.

### Naming standard

Append the word `Block` to the block name used in the schema documentation.

e.g. `Identifier` is mapped to type name `IdentifierBlock`, `Title` -> 
`TitleBlock`, etc.
  
### Capitalisation

Use pascal case for the block type name.

Initialisms and acronyms should be treated as proper words.

### Examples

* `IdentifierBlock`
* `TitleBlock`
* `AccessBlock`
* `AlternateUrlBlock`
* `RelatedRaidBlock`


### Pluralisation 

Stick to the singular, as used in the schema documentation.

### Examples
* use `TitleBlock`, not `TitlesBlock`


## Root fields

Talking here about fields at the root level of the meta schema, the fields that
contain the blocks.

### Naming standard

Use the block name for the field that contains the values of that block.

####
* use `identifier` 
  * not `Identifier` or `IdentifierBlock`
* use `title` 
  * not `tiles` or `Titles` or `titleBlocks`

### Pluralisation

Always use the singular.

####

* use `title`, not `titles`
* use `relatedRaid`, not `relatedRAiDs`

### Capitalisation

Use camel case.

#### Examples

* `identifier`
* `relatedRaid`
* `alternateUrl`


## Block fields

Talking here about fields within a block.

### Naming standard

Field names should be derived directly from the name in the schema 
documentation, including maintaining the "duplication" of the block name 
within the field name.

###$ Examples

* `IdentifierBlock`, stored in field named `identifier`
  * `identifier`
  * `identifierSchemeUri`
  * `identifierRegistrationAgency`
  * `identifierOwner`
  * `identifierServicePoint`

### Capitalisation

Use camel case.

#### Examples

* `IdentifierBlock`, stored in field named `identifier`
  * `identifier`
  * `identifierSchemeUri`
* `RelatedRaidBlock`, stored in field `relatedRaid`
  * `relatedRaid`
  * `relatedRaidType`
  * `relatedRaidTypeSchemeUri`

---

# Final example

```
{
  "metadataSchema": "RaidoMetadataSchemaV2",
  "identifier": {
    "identifier": "https://raid.org/prefix/suffix",
    "identifierSchemeUri": "https://raid.org",
    "identifierRegistrationAgency": "https://ror.org/038sjwq14",
    "identifierOwner": "https://ror.org/038sjwq14",
    "identifierServicePoint": 20000000,
  },
 "date": {
    "dateStart": "2023-03-08T00:00:00.000Z"
  },
  "title": [
    {
      "title": "sto mint 1",
      "titleType": "sto mint 1",
      "titleTypeSchemeUri": "Primary Title",
      "titleStartDate": "2023-03-08T00:00:00.000Z"
    }
  ],
  "contributor": [
    {
      "contributor": "https://orcid.org/0009-0004-9651-5072",
      "contributorIdentifierSchemeUri": "https://orcid.org/",
      "contributorPosition": [
        {
          "contributorPosition": "Leader",
          "contributorPositionSchemaUri": "https://raid.org/",
          "contributorPositionStartDate": "2023-03-08T00:00:00.000Z"
        }
      ],
      "contributorRole": [
        {
          "contributorRole": "project-administration"
          "contributorRoleSchemeUri": "https://credit.niso.org/",
        }
      ]
    }
  ],  
  "relatedRaid": [
    {
      "relatedRaid": "https://raid.org/prefix/suffix"
      "relatedRaidType": "https://github.com/au-research/raid-metadata/tree/main/scheme/related-raid/continues.json"
      "relatedRaidTypeSchemeUri": "https://github.com/au-research/raid-metadata/tree/main/scheme/related-raid",
    }
  ]
```