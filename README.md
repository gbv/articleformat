
# GBV Simple Article Schema Schema

```
https://uri.gbv.de/schema/article/01/schema#
```


| Abstract | Extensible | Status | Identifiable | Custom Properties | Additional Properties | Defined In |
|----------|------------|--------|--------------|-------------------|-----------------------|------------|
| Can be instantiated | No | Experimental | No | Forbidden | Permitted | [article_schema_fixed_arrays.schema.json](article_schema_fixed_arrays.schema.json) |

# GBV Simple Article Schema Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [abstracts](#abstracts) | `object[]` | Optional | GBV Simple Article Schema (this schema) |
| [copyright](#copyright) | `string` | Optional | GBV Simple Article Schema (this schema) |
| [fulltext_url](#fulltext_url) | `string` | Optional | GBV Simple Article Schema (this schema) |
| [journal](#journal) | `object` | **Required** | GBV Simple Article Schema (this schema) |
| [lang_code](#lang_code) | `string` | **Required** | GBV Simple Article Schema (this schema) |
| [other](#other) | `object` | Optional | GBV Simple Article Schema (this schema) |
| [other_ids](#other_ids) | `object[]` | Optional | GBV Simple Article Schema (this schema) |
| [persons](#persons) | `object[]` | Optional | GBV Simple Article Schema (this schema) |
| [primary_id](#primary_id) | `string` | **Required** | GBV Simple Article Schema (this schema) |
| [subject_terms](#subject_terms) | `object[]` | Optional | GBV Simple Article Schema (this schema) |
| [title](#title) | `string` | **Required** | GBV Simple Article Schema (this schema) |
| `*` | any | Additional | this schema *allows* additional properties |

## abstracts


`abstracts`

* is optional
* type: `object[]`
* defined in this schema

### abstracts Type


Array type: `object[]`

All items must be of the type:
`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `lang_code`| string | Optional |
| `text`| string | Optional |



#### lang_code

undefined

`lang_code`

* is optional
* type: `string`

##### lang_code Type


`string`









#### text

undefined

`text`

* is optional
* type: `string`

##### text Type


`string`















## copyright


`copyright`

* is optional
* type: `string`
* defined in this schema

### copyright Type


`string`







## fulltext_url


`fulltext_url`

* is optional
* type: `string`
* defined in this schema

### fulltext_url Type


`string`







## journal
### Zeitschrift

Quellenangabe

`journal`

* is **required**
* type: `object`
* defined in this schema

### journal Type


`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `coden`| string | Optional |
| `day`| string | Optional |
| `end_page`| string | Optional |
| `issue`| string | Optional |
| `journal_ids`|  | Optional |
| `month`| string | Optional |
| `place`| string | Optional |
| `publisher`| object | Optional |
| `start_page`| string | Optional |
| `title`| string | Optional |
| `volume`| string | Optional |
| `year`| string | Optional |



#### coden
##### Coden


`coden`

* is optional
* type: `string`

##### coden Type


`string`









#### day

undefined

`day`

* is optional
* type: `string`

##### day Type


`string`









#### end_page

undefined

`end_page`

* is optional
* type: `string`

##### end_page Type


`string`









#### issue

undefined

`issue`

* is optional
* type: `string`

##### issue Type


`string`









#### journal_ids

undefined

`journal_ids`

* is optional
* type: complex

##### journal_ids Type

Unknown type ``.

```json
{
  "simpletype": "complex"
}
```







#### month

undefined

`month`

* is optional
* type: `string`

##### month Type


`string`









#### place

undefined

`place`

* is optional
* type: `string`

##### place Type


`string`









#### publisher

undefined

`publisher`

* is optional
* type: `object`

##### publisher Type

Unknown type `object`.

```json
{
  "type": "object",
  "simpletype": "`object`"
}
```







#### start_page

undefined

`start_page`

* is optional
* type: `string`

##### start_page Type


`string`









#### title
##### Titel

Titel der Zeitschrift

`title`

* is optional
* type: `string`

##### title Type


`string`









#### volume

undefined

`volume`

* is optional
* type: `string`

##### volume Type


`string`









#### year

undefined

`year`

* is optional
* type: `string`

##### year Type


`string`












## lang_code


`lang_code`

* is **required**
* type: `string`
* defined in this schema

### lang_code Type


`string`







## other
### Anything else?

You may put one JSON object into the 'other' key for submitting additional data, that doesn't fit into the defined keys. You must put this data into a self-designed JSON object and you must provide a JSON schema for this JSON object. You should also provide a mapping of this JSON object to PICA fields.

`other`

* is optional
* type: `object`
* defined in this schema

### other Type


`object` with following properties:


| Property | Type | Required |
|----------|------|----------|






## other_ids
### weitere IDs

Weitere Identifier aus dem Quelldatensatz mit Angabe des Typs der ID, z.B. doi, urn, oai_id usw. (Frage: brauchen wir getrennte keys für andere IDs, die den Datensatz identifizieren, und IDs, die den Artikel identifizieren?)

`other_ids`

* is optional
* type: `object[]`
* defined in this schema

### other_ids Type


Array type: `object[]`

All items must be of the type:
`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `id`| string | **Required** |
| `type`| string | **Required** |



#### id
##### ID

Wert der ID

`id`

* is **required**
* type: `string`

##### id Type


`string`









#### type
##### Typ

Typ der ID

`type`

* is **required**
* type: `string`

##### type Type


`string`






##### type Examples

```json
doi
```

```json
oclc
```

```json
urn
```

```json
oai_id
```










## persons
### Personen

alle am Artikel beteiligten Personen

`persons`

* is optional
* type: `object[]`
* defined in this schema

### persons Type


Array type: `object[]`

All items must be of the type:
`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `affiliation`| object | Optional |
| `firstname`| string | Optional |
| `fullname`| string | **Required** |
| `lastname`| string | Optional |
| `person-ids`| array | Optional |
| `role`| string | Optional |



#### affiliation
##### Zugehörigkeit

Zugehörigkeit einer Person zu einer Einrichtung (z.B. Universität, Firma, Forschungseinrichtung usw.)

`affiliation`

* is optional
* type: `object`

##### affiliation Type

Unknown type `object`.

```json
{
  "type": "object",
  "title": "Zugehörigkeit",
  "description": "Zugehörigkeit einer Person zu einer Einrichtung (z.B. Universität, Firma, Forschungseinrichtung usw.)",
  "properties": {
    "name": {
      "type": "string",
      "title": "Name der Einrichrung",
      "description": "Name der Einrichtung"
    },
    "affiliation_ids": {
      "type": "array",
      "title": "Identifier der Einrichtung",
      "description": "Identifier, die die Einrichtung identifizieren",
      "items": {
        "type": "object",
        "required": [
          "id",
          "type"
        ],
        "properties": {
          "id": {
            "title": "ID",
            "description": "Wert der ID",
            "type": "string"
          },
          "type": {
            "title": "type",
            "description": "Typ der ID (z.B. gnd, viaf, ???)",
            "type": "string",
            "examples": [
              "gnd",
              "viaf"
            ]
          }
        }
      }
    }
  },
  "simpletype": "`object`"
}
```







#### firstname
##### Vorname

Vorname

`firstname`

* is optional
* type: `string`

##### firstname Type


`string`









#### fullname
##### Voller Name

persönlicher Name, dieser wird auch verwendet, wenn eine Aufteilung in Nachname, Vorname nicht möglich ist. Verfassende Organisationen (Körperschaften) können bei Aufsätzen auch als „persönlicher Name“ angegeben werden

`fullname`

* is **required**
* type: `string`

##### fullname Type


`string`









#### lastname
##### Nachname

Nachname

`lastname`

* is optional
* type: `string`

##### lastname Type


`string`









#### person-ids
##### ID der Person

Identifier, die die Person identifizieren (z.B. GND, ORCID, ...)

`person-ids`

* is optional
* type: `object[]`


##### person-ids Type


Array type: `object[]`

All items must be of the type:
`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `id`| string | **Required** |
| `type`| string | **Required** |



#### id
##### ID

Wert der ID

`id`

* is **required**
* type: `string`

##### id Type


`string`









#### type
##### Typ

Typ der ID (z.B. gnd, orcid, viaf, ...)

`type`

* is **required**
* type: `string`

##### type Type


`string`






##### type Examples

```json
orcid
```

```json
gnd
```












#### role
##### role

Roller der Person in Bezug auf den Artikel als relator code nach https://www.gbv.de/bibliotheken/verbundbibliotheken/02Verbund/01Erschliessung/02Richtlinien/02KatRichtRDA/anhaenge/anhang-beziehungskennzeichen

`role`

* is optional
* type: `string`

##### role Type


`string`






##### role Examples

```json
aut
```

```json
edt
```

```json
ill
```










## primary_id
### Primäre ID

primäre ID des Datensatzes in der Datenquelle

`primary_id`

* is **required**
* type: `string`
* defined in this schema

### primary_id Type


`string`







## subject_terms


`subject_terms`

* is optional
* type: `object[]`
* defined in this schema

### subject_terms Type


Array type: `object[]`

All items must be of the type:
`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `lang_code`| string | Optional |
| `scheme`| string | Optional |
| `terms`| array | Optional |



#### lang_code

undefined

`lang_code`

* is optional
* type: `string`

##### lang_code Type


`string`









#### scheme

undefined

`scheme`

* is optional
* type: `string`

##### scheme Type


`string`









#### terms

undefined

`terms`

* is optional
* type: `string[]`


##### terms Type


Array type: `string[]`

All items must be of the type:
`string`

















## title
### Titel

Der vollständige Titel des Artikels

`title`

* is **required**
* type: `string`
* defined in this schema

### title Type


`string`






