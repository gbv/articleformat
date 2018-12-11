
# Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG Schema

```
https://uri.gbv.de/schema/article/01/schema#
```

Dieses JSON-Schema (https://json-schema.org/) beschreibt ein JSON-Format zur Lieferung von bibliographischen Metadaten zu Zeitschriftenartikeln an die Verbundzentrale des GBV (VZG).

| Abstract | Extensible | Status | Identifiable | Custom Properties | Additional Properties | Defined In |
|----------|------------|--------|--------------|-------------------|-----------------------|------------|
| Can be instantiated | No | Experimental | No | Forbidden | Permitted | [article_schema.json](article_schema.json) |

# Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [abstracts](#abstracts) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [additional_data](#additional_data) | `object` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [copyright](#copyright) | `string` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [fulltext_url](#fulltext_url) | `string` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [journal](#journal) | `object` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [lang_code](#lang_code) | `string` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [other_ids](#other_ids) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [persons](#persons) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [primary_id](#primary_id) | `string` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [subject_terms](#subject_terms) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [title](#title) | `string` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| `*` | any | Additional | this schema *allows* additional properties |

## abstracts
### Abstracts, Zusammenfassungen usw.

Text mit Angabe der Sprache als Sprachcode aus ISO 639-2

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
##### Sprachcode

Sprachcode aus ISE 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV

`lang_code`

* is optional
* type: `string`

##### lang_code Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5Ba-z%5D%7B3%7D%24)):
```regex
^[a-z]{3}$
```








#### text
##### Text des Abstracts

undefined

`text`

* is optional
* type: `string`

##### text Type


`string`















## additional_data
### Sonst noch was?

In den key 'additional_data' kann ein JSON-Objekt mit weiteren Daten geschrieben werden. Dieses Objekt muss mit einem JSON-Schema spezifiziert sein und es sollte ein Mapping des Objekts auf Picaplus-Felder mitgeliefert werden.

`additional_data`

* is optional
* type: `object`
* defined in this schema

### additional_data Type


`object` with following properties:


| Property | Type | Required |
|----------|------|----------|






## copyright
### Copyrightvermerk

`copyright`

* is optional
* type: `string`
* defined in this schema

### copyright Type


`string`







## fulltext_url
### URL zum Volltext

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
| `end_page`| string | **Required** |
| `issue`| string | Optional |
| `journal_ids`| array | Optional |
| `month`| string | Optional |
| `place`| string | Optional |
| `publisher`| object | Optional |
| `start_page`| string | **Required** |
| `title`| string | **Required** |
| `volume`| string | Optional |
| `year`| string | **Required** |



#### coden
##### Coden

Hmmm, ist das nicht eine ID?

`coden`

* is optional
* type: `string`

##### coden Type


`string`









#### day
##### Tag

Tag des Erscheinens als zweistellige Zahl

`day`

* is optional
* type: `string`

##### day Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B0-9%5D%7B2%7D%24)):
```regex
^[0-9]{2}$
```








#### end_page
##### Endseite

undefined

`end_page`

* is **required**
* type: `string`

##### end_page Type


`string`









#### issue
##### Ausgabe

undefined

`issue`

* is optional
* type: `string`

##### issue Type


`string`









#### journal_ids
##### IDs der Zeitschrift

Identifier der Zeitschrift, z.B. E-ISSN, P-ISSN, ZDB-ID, publisher -ID usw.

`journal_ids`

* is optional
* type: `object[]`


##### journal_ids Type


Array type: `object[]`

All items must be of the type:
`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `id`| string | Optional |
| `type`| string | Optional |



#### id
##### ID

Wert der ID

`id`

* is optional
* type: `string`

##### id Type


`string`









#### type
##### Typ

Typ der ID, z.B. eissn, pissn, zdbid, springerid usw.

`type`

* is optional
* type: `string`

##### type Type


`string`






##### type Examples

```json
eissn
```

```json
pissn
```

```json
zdbid
```












#### month
##### Monat

Monat des Erscheinens als zweistellige Zahl

`month`

* is optional
* type: `string`

##### month Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B0-9%5D%7B2%7D%24)):
```regex
^[0-9]{2}$
```








#### place
##### Erscheinungsort

undefined

`place`

* is optional
* type: `string`

##### place Type


`string`









#### publisher
##### Verlag

Angaben zum Verlag, falls bekannt mit einem Identifier des Verlages (z.B. GND)

`publisher`

* is optional
* type: `object`

##### publisher Type

Unknown type `object`.

```json
{
  "type": "object",
  "title": "Verlag",
  "description": "Angaben zum Verlag, falls bekannt mit einem Identifier des Verlages (z.B. GND)",
  "properties": {
    "name": {
      "title": "Name des Verlages",
      "type": "string"
    },
    "publisher_ids": {
      "type": "array",
      "items": {
        "type": "object",
        "required": [
          "type",
          "id"
        ],
        "properties": {
          "id": {
            "title": "ID",
            "description": "Wert der ID",
            "type": "string"
          },
          "type": {
            "title": "Typ",
            "description": "Typ der ID, z.B. gnd",
            "type": "string",
            "examples": [
              "gnd"
            ]
          }
        }
      }
    }
  },
  "simpletype": "`object`"
}
```







#### start_page
##### Anfangsseite

undefined

`start_page`

* is **required**
* type: `string`

##### start_page Type


`string`









#### title
##### Titel

Titel der Zeitschrift

`title`

* is **required**
* type: `string`

##### title Type


`string`









#### volume
##### Band

undefined

`volume`

* is optional
* type: `string`

##### volume Type


`string`









#### year
##### Erscheinungsjahr

Erscheinungsjahr als vierstellige Zahl

`year`

* is **required**
* type: `string`

##### year Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B0-9%5D%7B4%7D%24)):
```regex
^[0-9]{4}$
```











## lang_code
### Sprache

Sprachcode aus ISE 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV

`lang_code`

* is **required**
* type: `string`
* defined in this schema

### lang_code Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5Ba-z%5D%7B3%7D%24)):
```regex
^[a-z]{3}$
```






## other_ids
### weitere IDs

Weitere Identifier aus dem Quelldatensatz mit Angabe des Typs der ID, z.B. doi, urn, oai_id usw. Vergleiche http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=2113&regelwerk=RDA&verbund=GBV

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

alle am Artikel beteiligten Personen in der Reihenfolge der Nennung im Artikel

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
      "title": "Name der Einrichtung",
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
##### IDs der Person

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

Rolle der Person in Bezug auf den Artikel als relator code nach https://www.gbv.de/bibliotheken/verbundbibliotheken/02Verbund/01Erschliessung/02Richtlinien/02KatRichtRDA/anhaenge/anhang-beziehungskennzeichen

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
### Sacherschließung

Mit Angabe des Sacherschließungssystems und der Sprache als Sprachcode aus ISO 639-2

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
| `scheme`| string | **Required** |
| `terms`| array | **Required** |



#### lang_code
##### Sprachcode

Sprachcode aus ISE 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV

`lang_code`

* is optional
* type: `string`

##### lang_code Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5Ba-z%5D%7B3%7D%24)):
```regex
^[a-z]{3}$
```








#### scheme
##### Sacherschließungssystem

Bezeichnung des Sacherschließungssystems

`scheme`

* is **required**
* type: `string`

##### scheme Type


`string`









#### terms
##### Sacherschließungsterme

Sacherschließungsterme als Array, jeder Term als eigenes Feld

`terms`

* is **required**
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






