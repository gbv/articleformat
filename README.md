
# Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG Schema

```
https://uri.gbv.de/schema/article/01/schema#
```

Dieses JSON-Schema (https://json-schema.org/) beschreibt ein JSON-Format zur Lieferung von bibliographischen Metadaten zu Zeitschriftenartikeln an die Verbundzentrale des GBV (VZG). HTML-Dokumentation: http://findex.gbv.de/articleformatdoc/schemas/article_schema.html

| Abstract | Extensible | Status | Identifiable | Custom Properties | Additional Properties | Defined In |
|----------|------------|--------|--------------|-------------------|-----------------------|------------|
| Can be instantiated | Yes | Experimental | No | Forbidden | Permitted | [article_schema.json](article_schema.json) |

# Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [abstracts](#abstracts) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [additional_data](#additional_data) | `object` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [copyright](#copyright) | `string` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [journal](#journal) | `object` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [lang_code](#lang_code) | `string[]` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [otherTitles](#othertitles) | `string[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [other_ids](#other_ids) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [persons](#persons) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [primary_id](#primary_id) | `object` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [relatedWorks](#relatedworks) | reference | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [subTitle](#subtitle) | `string` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [subject_terms](#subject_terms) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [title](#title) | `string` | **Required** | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
| [urls](#urls) | `object[]` | Optional | Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG (this schema) |
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
| `text`| string | **Required** |



#### lang_code
##### Sprachcode

Sprachcode aus ISO 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV

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

* is **required**
* type: `string`

##### text Type


`string`

* minimum length: 1 characters













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

* minimum length: 1 characters





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
| `day`| string | Optional |
| `end_page`| string | Optional |
| `issue`| string | Optional |
| `journal_ids`| array | Optional |
| `month`| string | Optional |
| `place`| string | Optional |
| `publisher`| object | Optional |
| `start_page`| string | Optional |
| `title`| string | **Required** |
| `volume`| string | Optional |
| `year`| string | **Required** |



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

* is optional
* type: `string`

##### end_page Type


`string`

* minimum length: 1 characters







#### issue
##### Ausgabe

undefined

`issue`

* is optional
* type: `string`

##### issue Type


`string`

* minimum length: 1 characters







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

* minimum length: 1 characters







#### type
##### Typ

Typ der ID, z.B. CODEN, eissn, pissn, zdbid, springerid usw. Falls unkbekannt: unknown

`type`

* is optional
* type: `string`

##### type Type


`string`

* minimum length: 1 characters




##### type Examples

```json
coden
```

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

* minimum length: 1 characters







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
      "type": "string",
      "minLength": 1
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
            "type": "string",
            "minLength": 1
          },
          "type": {
            "title": "Typ",
            "description": "Typ der ID, z.B. gnd. Falls unkbekannt: unknown",
            "type": "string",
            "minLength": 1,
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

* is optional
* type: `string`

##### start_page Type


`string`

* minimum length: 1 characters







#### title
##### Titel

Titel der Zeitschrift

`title`

* is **required**
* type: `string`

##### title Type


`string`

* minimum length: 1 characters







#### volume
##### Band

undefined

`volume`

* is optional
* type: `string`

##### volume Type


`string`

* minimum length: 1 characters







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
### Sprache(n)

Sprachcode(s) aus ISO 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV

`lang_code`

* is **required**
* type: `string[]`
* defined in this schema

### lang_code Type


Array type: `string[]`

All items must be of the type:
`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5Ba-z%5D%7B3%7D%24)):
```regex
^[a-z]{3}$
```









## otherTitles
### Weitere Titel

Weitere Titelformen

`otherTitles`

* is optional
* type: `string[]`
* defined in this schema

### otherTitles Type


Array type: `string[]`

All items must be of the type:
`string`

* minimum length: 1 characters








## other_ids
### weitere IDs

Weitere Identifier aus dem Quelldatensatz mit Angabe des Typs der ID, z.B. doi, urn, oai_id usw. (hier keine Identifier zu Zeitschriften, Personen usw.) Vergleiche http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=2113&regelwerk=RDA&verbund=GBV

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

* minimum length: 1 characters







#### type
##### Typ

Typ der ID. Falls unkbekannt: unknown

`type`

* is **required**
* type: `string`

##### type Type


`string`

* minimum length: 1 characters




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
| `person_ids`| array | Optional |
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
      "description": "Name der Einrichtung",
      "minLength": 1
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
            "type": "string",
            "minLength": 1
          },
          "type": {
            "title": "type",
            "description": "Typ der ID (z.B. gnd, viaf, ???). Falls unkbekannt: unknown",
            "type": "string",
            "minLength": 1,
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

* minimum length: 1 characters







#### fullname
##### Voller Name

persönlicher Name, dieser wird auch verwendet, wenn eine Aufteilung in Nachname, Vorname nicht möglich ist. Verfassende Organisationen (Körperschaften) können bei Aufsätzen auch als „persönlicher Name“ angegeben werden

`fullname`

* is **required**
* type: `string`

##### fullname Type


`string`

* minimum length: 1 characters







#### lastname
##### Nachname

Nachname

`lastname`

* is optional
* type: `string`

##### lastname Type


`string`

* minimum length: 1 characters







#### person_ids
##### IDs der Person

Identifier, die die Person identifizieren (z.B. GND, ORCID, ...)

`person_ids`

* is optional
* type: `object[]`


##### person_ids Type


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

* minimum length: 1 characters







#### type
##### Typ

Typ der ID (z.B. gnd, orcid, viaf, ...). Falls unkbekannt: unknown

`type`

* is **required**
* type: `string`

##### type Type


`string`

* minimum length: 1 characters




##### type Examples

```json
orcid
```

```json
gnd
```












#### role
##### role

Rolle der Person in Bezug auf den Artikel als relator code nach https://opus.k10plus.de/frontdoor/deliver/index/docId/421/file/Liste_Beziehungskennzeichnungen_3010_3110.pdf

`role`

* is optional
* type: `string`

##### role Type


`string`

* minimum length: 1 characters




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


`primary_id`

* is **required**
* type: `object`
* defined in this schema

### primary_id Type


`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `id`| string | **Required** |
| `type`| string | **Required** |



#### id
##### Primäre ID

primäre ID des Datensatzes in der Datenquelle

`id`

* is **required**
* type: `string`

##### id Type


`string`

* minimum length: 1 characters







#### type
##### Typ

Typ der ID. Der Typ der ID sollte so gewählt werden, dass nachvollziehbar ist, woher die Datensätze stammen. Die Katalogiserungsrichtlinie schlägt in den 20XX- und 21XX-Feldern Kürzel für einige Datenlieferanten vor, die auch hier genutzt werden sollten: http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=index&regelwerk=RDA&verbund=GBV#titel . Falls unkbekannt: unknown

`type`

* is **required**
* type: `string`

##### type Type


`string`

* minimum length: 1 characters




##### type Examples

```json
oai_id
```

```json
https://kxp.k10plus.de/DB=2.1/
```

```json
oclc
```








## relatedWorks
### Weitere Veröffentlichungen

Hier können im gleichen Format zu 'journal' weitere Verknüpfungen untergebracht werden.

`relatedWorks`

* is optional
* type: reference
* defined in this schema

### relatedWorks Type


Array type: reference

All items must be of the type:
* []() – `#/definitions/journal`








## subTitle
### Titel

Eventuelle Ergänzung zum Haupttitel

`subTitle`

* is optional
* type: `string`
* defined in this schema

### subTitle Type


`string`

* minimum length: 1 characters





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

Sprachcode aus ISO 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV

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

* minimum length: 1 characters







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

* minimum length: 1 characters















## title
### Titel

Der Haupttitel des Artikels

`title`

* is **required**
* type: `string`
* defined in this schema

### title Type


`string`

* minimum length: 1 characters





## urls
### URLs zum Artikel

URLs zum Artikel mit Angabe zum 'Bezugswerk' in 'scope' sowie zu Benutzungsbedingungen in 'access_info'

`urls`

* is optional
* type: `object[]`
* defined in this schema

### urls Type


Array type: `object[]`

All items must be of the type:
`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `access_info`| string | **Required** |
| `scope`| string | **Required** |
| `url`| string | **Required** |



#### access_info
##### Codierte Zugangsbedingungen

Hier werden Zugangsbedingungen (z.B. Open Access) codiert gemäß Katalogisierungsrichtlinie für PICA3 4085 $4: http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=4085&regelwerk=RDA&verbund=GBV#$4

`access_info`

* is **required**
* type: `string`

##### access_info Type


`string`









#### scope
##### Bezugswerk

Hier sollen insbesondere URLs zum Volltext des Artikels, aber auch alle anderen Arten von 'Linkzielen' nach Typ codiert werden mit ONIX-Codes gemäß Katalogisierungsrichtlinie für PICA3-Feld 4085 $3: http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=4085&regelwerk=RDA&verbund=GBV#$3

`scope`

* is **required**
* type: `string`

##### scope Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%24%7C%5E%5B0-9%5D%5B0-9%5D%24)):
```regex
^$|^[0-9][0-9]$
```








#### url
##### URL

undefined

`url`

* is **required**
* type: `string`

##### url Type


`string`

* minimum length: 1 characters













# Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG Definitions

| Property | Type | Group |
|----------|------|-------|
| [day](#day) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [end_page](#end_page) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [issue](#issue) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [journal_ids](#journal_ids) | `object[]` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [month](#month) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [place](#place) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [publisher](#publisher) | `object` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [start_page](#start_page) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [volume](#volume) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |
| [year](#year) | `string` | `https://uri.gbv.de/schema/article/01/schema##/definitions/journal` |

## day
### Tag

Tag des Erscheinens als zweistellige Zahl

`day`

* is optional
* type: `string`
* defined in this schema

### day Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B0-9%5D%7B2%7D%24)):
```regex
^[0-9]{2}$
```






## end_page
### Endseite

`end_page`

* is optional
* type: `string`
* defined in this schema

### end_page Type


`string`

* minimum length: 1 characters





## issue
### Ausgabe

`issue`

* is optional
* type: `string`
* defined in this schema

### issue Type


`string`

* minimum length: 1 characters





## journal_ids
### IDs der Zeitschrift

Identifier der Zeitschrift, z.B. E-ISSN, P-ISSN, ZDB-ID, publisher -ID usw.

`journal_ids`

* is optional
* type: `object[]`
* defined in this schema

### journal_ids Type


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

* minimum length: 1 characters







#### type
##### Typ

Typ der ID, z.B. CODEN, eissn, pissn, zdbid, springerid usw. Falls unkbekannt: unknown

`type`

* is optional
* type: `string`

##### type Type


`string`

* minimum length: 1 characters




##### type Examples

```json
coden
```

```json
eissn
```

```json
pissn
```

```json
zdbid
```










## month
### Monat

Monat des Erscheinens als zweistellige Zahl

`month`

* is optional
* type: `string`
* defined in this schema

### month Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B0-9%5D%7B2%7D%24)):
```regex
^[0-9]{2}$
```






## place
### Erscheinungsort

`place`

* is optional
* type: `string`
* defined in this schema

### place Type


`string`

* minimum length: 1 characters





## publisher
### Verlag

Angaben zum Verlag, falls bekannt mit einem Identifier des Verlages (z.B. GND)

`publisher`

* is optional
* type: `object`
* defined in this schema

### publisher Type


`object` with following properties:


| Property | Type | Required |
|----------|------|----------|
| `name`| string | Optional |
| `publisher_ids`| array | Optional |



#### name
##### Name des Verlages

undefined

`name`

* is optional
* type: `string`

##### name Type


`string`

* minimum length: 1 characters







#### publisher_ids

undefined

`publisher_ids`

* is optional
* type: `object[]`


##### publisher_ids Type


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

* minimum length: 1 characters







#### type
##### Typ

Typ der ID, z.B. gnd. Falls unkbekannt: unknown

`type`

* is **required**
* type: `string`

##### type Type


`string`

* minimum length: 1 characters




##### type Example

```json
gnd
```














## start_page
### Anfangsseite

`start_page`

* is optional
* type: `string`
* defined in this schema

### start_page Type


`string`

* minimum length: 1 characters





## volume
### Band

`volume`

* is optional
* type: `string`
* defined in this schema

### volume Type


`string`

* minimum length: 1 characters





## year
### Erscheinungsjahr

Erscheinungsjahr als vierstellige Zahl

`year`

* is optional
* type: `string`
* defined in this schema

### year Type


`string`



All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B0-9%5D%7B4%7D%24)):
```regex
^[0-9]{4}$
```





