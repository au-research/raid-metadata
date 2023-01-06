# 1 Identifier

**Occurance:** 1
**Definition:** The Identifier is a unique string that identifies a resource.
**Allowed values, examples, other constraints:** 

_RAiD (Research Activity Identifier) registered by a RAiD Registration Agency._

**Requirement:** Mandatory
**Schema block:** Core-ID
**Notes:**

### 1a identifierSchemeURI

**Occurance:** 1
**Definition:** The URI of the Identifier scheme.
**Allowed values, examples, other constraints:** 

- [https://raid.org](https://raid.org)

**Requirement:** Mandatory
**Schema block:** Core-ID
**Notes:** This Property declares that the Identifier is a RAiD.

## 1.1 identifierRegistrationAgency

**Occurance:** 1
**Definition:** The Registration Agency that minted the RAiD.
**Allowed values, examples, other constraints:** 

_List of Registration Agency RORs (e.g., for ARDC, JISC, SURF, etc.)._

**Requirement:** Mandatory
**Schema block:** Core-ID
**Notes:** Registration Agencies must have or acquire RORs.



