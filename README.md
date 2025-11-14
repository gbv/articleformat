# Ein einfaches Schema zur Lieferung von Daten zu Zeitschriftenartikeln an die VZG

*Dieses JSON-Schema (https://json-schema.org/) beschreibt ein JSON-Format zur Lieferung von bibliographischen Metadaten zu Zeitschriftenartikeln an die Verbundzentrale des GBV (VZG). HTML-Dokumentation: http://findex.gbv.de/articleformatdoc/schemas/article_schema.html*

Type: `object`

<i id="httpsuri.gbv.deschemaarticle01schema">path: #https://uri.gbv.de/schema/article/01/schema#</i>

&#36;schema: [http://json-schema.org/draft-07/schema#](http://json-schema.org/draft-07/schema#)

<b id="httpsuri.gbv.deschemaarticle01schema">&#36;id: https://uri.gbv.de/schema/article/01/schema#</b>

***Properties***

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesprimary-id">primary_id</b> `required`
	 - Type: `object`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesprimary-id">path: #https://uri.gbv.de/schema/article/01/schema#/properties/primary_id</i>
	 - ***Properties***
		 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesprimary-idpropertiesid">id</b> `required`
			 - ##### Primäre ID
			 - *primäre ID des Datensatzes in der Datenquelle*
			 - Type: `string`
			 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesprimary-idpropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/properties/primary_id/properties/id</i>
			 - Length:  &ge; 1

		 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesprimary-idpropertiestype">type</b> `required`
			 - ##### Typ
			 - *Typ der ID. Der Typ der ID sollte so gewählt werden, dass nachvollziehbar ist, woher die Datensätze stammen. Die Katalogiserungsrichtlinie schlägt in den 20XX- und 21XX-Feldern Kürzel für einige Datenlieferanten vor, die auch hier genutzt werden sollten: http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=index&regelwerk=RDA&verbund=GBV#titel . Falls unkbekannt: unknown*
			 - Type: `string`
			 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesprimary-idpropertiestype">path: #https://uri.gbv.de/schema/article/01/schema#/properties/primary_id/properties/type</i>
			 - Example values: 
				 1. *"oai_id"*
				 2. *"https://kxp.k10plus.de/DB=2.1/"*
				 3. *"oclc"*
			 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesother-ids">other_ids</b>
	 - ### weitere IDs
	 - *Weitere Identifier für den Artikel aus dem Quelldatensatz mit Angabe des Typs der ID, z.B. doi, urn, oai_id usw. (hier keine Identifier zu Zeitschriften, Personen usw.) Vergleiche http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=2113&regelwerk=RDA&verbund=GBV*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesother-ids">path: #https://uri.gbv.de/schema/article/01/schema#/properties/other_ids</i>
		 - ***Items***
		 - Type: `object`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesother-idsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/other_ids/items</i>
		 - ***Properties***
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesother-idsitemspropertiesid">id</b> `required`
				 - ##### ID
				 - *Wert der ID*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesother-idsitemspropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/properties/other_ids/items/properties/id</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesother-idsitemspropertiestype">type</b> `required`
				 - ##### Typ
				 - *Typ der ID. Falls unkbekannt: unknown*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesother-idsitemspropertiestype">path: #https://uri.gbv.de/schema/article/01/schema#/properties/other_ids/items/properties/type</i>
				 - Example values: 
					 1. *"doi"*
					 2. *"oclc"*
					 3. *"urn"*
					 4. *"oai_id"*
				 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiescollection-ids">collection_ids</b>
	 - ### IDs von Datensammlungen
	 - *Datensätze können über diese IDs bestehenden Datensammlungen zugeordnet werden. Verwendung bitte je Projekt mit der Verbundzentrale (VZG) abklären. Beispiele: SSG-Nummer/FID-Kennzeichen, Produktsigel usw.*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiescollection-ids">path: #https://uri.gbv.de/schema/article/01/schema#/properties/collection_ids</i>
		 - ***Items***
		 - Type: `object`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiescollection-idsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/collection_ids/items</i>
		 - ***Properties***
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiescollection-idsitemspropertiesid">id</b> `required`
				 - ##### ID
				 - *Wert der ID*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiescollection-idsitemspropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/properties/collection_ids/items/properties/id</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiescollection-idsitemspropertiestype">type</b> `required`
				 - ##### Typ
				 - *Typ der ID. Falls unkbekannt: unknown*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiescollection-idsitemspropertiestype">path: #https://uri.gbv.de/schema/article/01/schema#/properties/collection_ids/items/properties/type</i>
				 - Example values: 
					 1. *"sigel"*
					 2. *"fid"*
					 3. *"ssg"*
				 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiestitle">title</b> `required`
	 - ### Titel
	 - *Der Haupttitel des Artikels*
	 - Type: `string`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiestitle">path: #https://uri.gbv.de/schema/article/01/schema#/properties/title</i>
	 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiessubtitle">subTitle</b>
	 - ### Titel
	 - *Eventuelle Ergänzung zum Haupttitel*
	 - Type: `string`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubtitle">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subTitle</i>
	 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesothertitles">otherTitles</b>
	 - ### Weitere Titel
	 - *Weitere Titelformen*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesothertitles">path: #https://uri.gbv.de/schema/article/01/schema#/properties/otherTitles</i>
		 - ***Items***
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesothertitlesitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/otherTitles/items</i>
		 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersons">persons</b>
	 - ### Personen
	 - *alle am Artikel beteiligten Personen in der Reihenfolge der Nennung im Artikel*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersons">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons</i>
		 - ***Items***
		 - Type: `object`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items</i>
		 - ***Properties***
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesfullname">fullname</b> `required`
				 - ##### Voller Name
				 - *persönlicher Name, dieser wird auch verwendet, wenn eine Aufteilung in Nachname, Vorname nicht möglich ist. Verfassende Organisationen (Körperschaften) können bei Aufsätzen auch als „persönlicher Name“ angegeben werden*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesfullname">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/fullname</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesfirstname">firstname</b>
				 - ##### Vorname
				 - *Vorname*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesfirstname">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/firstname</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertieslastname">lastname</b>
				 - ##### Nachname
				 - *Nachname*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertieslastname">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/lastname</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesrole">role</b>
				 - ##### role
				 - *Rolle der Person in Bezug auf den Artikel als relator code nach https://opus.k10plus.de/frontdoor/deliver/index/docId/421/file/Liste_Beziehungskennzeichnungen_3010_3110.pdf*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesrole">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/role</i>
				 - Example values: 
					 1. *"aut"*
					 2. *"edt"*
					 3. *"ill"*
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliation">affiliation</b>
				 - ##### Zugehörigkeit
				 - *Zugehörigkeit einer Person zu einer Einrichtung (z.B. Universität, Firma, Forschungseinrichtung usw.)*
				 - Type: `object`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliation">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/affiliation</i>
				 - ***Properties***
					 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesname">name</b>
						 - ##### Name der Einrichtung
						 - *Name der Einrichtung*
						 - Type: `string`
						 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesname">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/affiliation/properties/name</i>
						 - Length:  &ge; 1

					 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesaffiliation-ids">affiliation_ids</b>
						 - ##### Identifier der Einrichtung
						 - *Identifier, die die Einrichtung identifizieren*
						 - Type: `array`
						 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesaffiliation-ids">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/affiliation/properties/affiliation_ids</i>
							 - ***Items***
							 - Type: `object`
							 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesaffiliation-idsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/affiliation/properties/affiliation_ids/items</i>
							 - ***Properties***
								 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesaffiliation-idsitemspropertiesid">id</b> `required`
									 - ##### ID
									 - *Wert der ID*
									 - Type: `string`
									 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesaffiliation-idsitemspropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/affiliation/properties/affiliation_ids/items/properties/id</i>
									 - Length:  &ge; 1

								 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesaffiliation-idsitemspropertiestype">type</b> `required`
									 - ##### type
									 - *Typ der ID (z.B. gnd, viaf, ???). Falls unkbekannt: unknown*
									 - Type: `string`
									 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesaffiliationpropertiesaffiliation-idsitemspropertiestype">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/affiliation/properties/affiliation_ids/items/properties/type</i>
									 - Example values: 
										 1. *"gnd"*
										 2. *"viaf"*
									 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesperson-ids">person_ids</b>
				 - ##### IDs der Person
				 - *Identifier, die die Person identifizieren (z.B. GND, ORCID, ...)*
				 - Type: `array`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesperson-ids">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/person_ids</i>
					 - ***Items***
					 - Type: `object`
					 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesperson-idsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/person_ids/items</i>
					 - ***Properties***
						 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesperson-idsitemspropertiesid">id</b> `required`
							 - ##### ID
							 - *Wert der ID*
							 - Type: `string`
							 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesperson-idsitemspropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/person_ids/items/properties/id</i>
							 - Length:  &ge; 1

						 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesperson-idsitemspropertiestype">type</b> `required`
							 - ##### Typ
							 - *Typ der ID (z.B. gnd, orcid, viaf, ...). Falls unkbekannt: unknown*
							 - Type: `string`
							 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiespersonsitemspropertiesperson-idsitemspropertiestype">path: #https://uri.gbv.de/schema/article/01/schema#/properties/persons/items/properties/person_ids/items/properties/type</i>
							 - Example values: 
								 1. *"orcid"*
								 2. *"gnd"*
							 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesjournal">journal</b> `required`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesjournal">path: #https://uri.gbv.de/schema/article/01/schema#/properties/journal</i>
	 - &#36;ref: [#/definitions/journal](#/definitions/journal)
 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesrelatedworks">relatedWorks</b>
	 - ### Weitere Veröffentlichungen
	 - *Hier können im gleichen Format zu 'journal' weitere Verknüpfungen untergebracht werden.*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesrelatedworks">path: #https://uri.gbv.de/schema/article/01/schema#/properties/relatedWorks</i>
		 - ***Items***
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesrelatedworksitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/relatedWorks/items</i>
		 - &#36;ref: [#/definitions/journal](#/definitions/journal)
 - <b id="httpsuri.gbv.deschemaarticle01schemapropertieslang-code">lang_code</b> `required`
	 - ### Sprache(n)
	 - *Sprachcode(s) aus ISO 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertieslang-code">path: #https://uri.gbv.de/schema/article/01/schema#/properties/lang_code</i>
		 - ***Items***
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertieslang-codeitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/lang_code/items</i>
		 - The value must match this pattern: `^[a-z]{3}$`
 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesurls">urls</b>
	 - ### URLs zum Artikel
	 - *URLs zum Artikel mit Angabe zum 'Bezugswerk' in 'scope' sowie zu Benutzungsbedingungen in 'access_info'*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesurls">path: #https://uri.gbv.de/schema/article/01/schema#/properties/urls</i>
		 - ***Items***
		 - Type: `object`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/urls/items</i>
		 - ***Properties***
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesurl">url</b> `required`
				 - ##### URL
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesurl">path: #https://uri.gbv.de/schema/article/01/schema#/properties/urls/items/properties/url</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesscope">scope</b> `required`
				 - ##### Bezugswerk
				 - *Hier sollen insbesondere URLs zum Volltext des Artikels, aber auch alle anderen Arten von 'Linkzielen' nach Typ codiert werden mit ONIX-Codes gemäß Katalogisierungsrichtlinie für PICA3-Feld 4085 $3: http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=4085&regelwerk=RDA&verbund=GBV#$3*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesscope">path: #https://uri.gbv.de/schema/article/01/schema#/properties/urls/items/properties/scope</i>
				 - The value must match this pattern: `^$|^[0-9][0-9]$`
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesaccess-info">access_info</b> `required`
				 - ##### Codierte Zugangsbedingungen
				 - *Hier werden Zugangsbedingungen (z.B. Open Access) codiert gemäß Katalogisierungsrichtlinie für PICA3 4085 $4: http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=4085&regelwerk=RDA&verbund=GBV#$4*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesaccess-info">path: #https://uri.gbv.de/schema/article/01/schema#/properties/urls/items/properties/access_info</i>
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesremarks">remarks</b>
				 - ##### Allgemeine Bemerkung
				 - *Bemerkungen zur URL als Text, die in PICA3-Feld 4950 $z abgelegt werden*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesurlsitemspropertiesremarks">path: #https://uri.gbv.de/schema/article/01/schema#/properties/urls/items/properties/remarks</i>
 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesabstracts">abstracts</b>
	 - ### Abstracts, Zusammenfassungen usw.
	 - *Text mit Angabe der Sprache als Sprachcode aus ISO 639-2*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesabstracts">path: #https://uri.gbv.de/schema/article/01/schema#/properties/abstracts</i>
		 - ***Items***
		 - Type: `object`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesabstractsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/abstracts/items</i>
		 - ***Properties***
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesabstractsitemspropertiestext">text</b> `required`
				 - ##### Text des Abstracts
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesabstractsitemspropertiestext">path: #https://uri.gbv.de/schema/article/01/schema#/properties/abstracts/items/properties/text</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesabstractsitemspropertieslang-code">lang_code</b>
				 - ##### Sprachcode
				 - *Sprachcode aus ISO 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesabstractsitemspropertieslang-code">path: #https://uri.gbv.de/schema/article/01/schema#/properties/abstracts/items/properties/lang_code</i>
				 - The value must match this pattern: `^[a-z]{3}$`
 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-terms">subject_terms</b>
	 - ### Sacherschließung
	 - *Mit Angabe des Sacherschließungssystems und der Sprache als Sprachcode aus ISO 639-2*
	 - Type: `array`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-terms">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms</i>
		 - ***Items***
		 - Type: `object`
		 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms/items</i>
		 - ***Properties***
			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiesterms">terms</b> `required`
				 - ##### Sacherschließungsterme
				 - *Sacherschließungsterme als Array. Entweder jeder Term als eigenes String-Feld; oder als Objekt bestehend aus einer Bezeichnung und einer ID oder Notation (z.B. GND-ID)*
				 - Type: `array`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiesterms">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms/items/properties/terms</i>
					 - ***Items***
					 - Types: `string`, `object`
					 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiestermsitems">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms/items/properties/terms/items</i>
					 - Length:  &ge; 1

					 - Property Count:  &ge; 1

					 - ***Properties***
						 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiestermsitemspropertiesterm">term</b>
							 - ##### Term/Bezeichnung
							 - Type: `string`
							 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiestermsitemspropertiesterm">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms/items/properties/terms/items/properties/term</i>
							 - Length:  &ge; 1

						 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiestermsitemspropertiesid">id</b>
							 - ##### Identifikator/Notation innerhalb des Sacherschließungssystems
							 - Type: `string`
							 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiestermsitemspropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms/items/properties/terms/items/properties/id</i>
							 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiesscheme">scheme</b> `required`
				 - ##### Sacherschließungssystem
				 - *Bezeichnung des Sacherschließungssystems*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertiesscheme">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms/items/properties/scheme</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertieslang-code">lang_code</b>
				 - ##### Sprachcode
				 - *Sprachcode aus ISO 639-2. Zur Verwendung siehe http://swbtools.bsz-bw.de/cgi-bin/help.pl?cmd=kat&val=1500&regelwerk=RDA&verbund=GBV*
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiessubject-termsitemspropertieslang-code">path: #https://uri.gbv.de/schema/article/01/schema#/properties/subject_terms/items/properties/lang_code</i>
				 - The value must match this pattern: `^[a-z]{3}$`
 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiescopyright">copyright</b>
	 - ### Copyrightvermerk
	 - Type: `string`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiescopyright">path: #https://uri.gbv.de/schema/article/01/schema#/properties/copyright</i>
	 - Length:  &ge; 1

 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesdateofproduction">dateOfProduction</b>
	 - ### Herstellungsdatum
	 - *Herstellungsdatum (z.B. Datum der Digitalisierung). Das Datum kann als vierstelliges Jahr (YYYY), Jahr und Monat (YYYY-MM) oder Jahr, Monat und Tag (YYYY-MM-DD) angegeben werden. s.a. PICA 1108 $p: https://swbtools.bsz-bw.de/cgi-bin/k10plushelp.pl?cmd=kat&val=1108&katalog=Standard*
	 - Type: `string`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesdateofproduction">path: #https://uri.gbv.de/schema/article/01/schema#/properties/dateOfProduction</i>
	 - The value must match this pattern: `^[0-9]{4}(-[0-9]{2}){0,2}$`
 - <b id="httpsuri.gbv.deschemaarticle01schemapropertiesadditional-data">additional_data</b>
	 - ### Sonst noch was?
	 - *In den key 'additional_data' kann ein JSON-Objekt mit weiteren Daten geschrieben werden. Dieses Objekt muss mit einem JSON-Schema spezifiziert sein und es sollte ein Mapping des Objekts auf Picaplus-Felder mitgeliefert werden.*
	 - Type: `object`
	 - <i id="httpsuri.gbv.deschemaarticle01schemapropertiesadditional-data">path: #https://uri.gbv.de/schema/article/01/schema#/properties/additional_data</i>
	 - ***Properties***
# definitions

***journal***

 - ## Zeitschrift
 - *Quellenangabe*
 - Type: `object`
 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournal">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal</i>
 - ***Properties***
	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiestitle">title</b> `required`
		 - #### Titel
		 - *Titel der Zeitschrift*
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiestitle">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/title</i>
		 - Length:  &ge; 1

	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesjournal-ids">journal_ids</b>
		 - #### IDs der Zeitschrift
		 - *Identifier der Zeitschrift, z.B. E-ISSN, P-ISSN, ZDB-ID, publisher -ID usw.*
		 - Type: `array`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesjournal-ids">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/journal_ids</i>
			 - ***Items***
			 - Type: `object`
			 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesjournal-idsitems">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/journal_ids/items</i>
			 - ***Properties***
				 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesjournal-idsitemspropertiesid">id</b> `required`
					 - ##### ID
					 - *Wert der ID*
					 - Type: `string`
					 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesjournal-idsitemspropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/journal_ids/items/properties/id</i>
					 - Length:  &ge; 1

				 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesjournal-idsitemspropertiestype">type</b> `required`
					 - ##### Typ
					 - *Typ der ID, z.B. CODEN, eissn, pissn, zdbid, springerid usw. Falls unkbekannt: unknown*
					 - Type: `string`
					 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesjournal-idsitemspropertiestype">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/journal_ids/items/properties/type</i>
					 - Example values: 
						 1. *"coden"*
						 2. *"eissn"*
						 3. *"pissn"*
						 4. *"zdbid"*
					 - Length:  &ge; 1

	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesyear">year</b> `required`
		 - #### Erscheinungsjahr
		 - *Erscheinungsjahr als vierstellige Zahl*
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesyear">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/year</i>
		 - The value must match this pattern: `^[0-9]{4}$`
	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesmonth">month</b>
		 - #### Monat
		 - *Monat des Erscheinens als zweistellige Zahl*
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesmonth">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/month</i>
		 - The value must match this pattern: `^[0-9]{2}$`
	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesday">day</b>
		 - #### Tag
		 - *Tag des Erscheinens als zweistellige Zahl*
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesday">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/day</i>
		 - The value must match this pattern: `^[0-9]{2}$`
	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesvolume">volume</b>
		 - #### Band
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesvolume">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/volume</i>
		 - Length:  &ge; 1

	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesissue">issue</b>
		 - #### Ausgabe
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesissue">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/issue</i>
		 - Length:  &ge; 1

	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisher">publisher</b>
		 - #### Verlag
		 - *Angaben zum Verlag, falls bekannt mit einem Identifier des Verlages (z.B. GND)*
		 - Type: `object`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisher">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/publisher</i>
		 - ***Properties***
			 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiesname">name</b>
				 - ##### Name des Verlages
				 - Type: `string`
				 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiesname">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/publisher/properties/name</i>
				 - Length:  &ge; 1

			 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiespublisher-ids">publisher_ids</b>
				 - Type: `array`
				 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiespublisher-ids">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/publisher/properties/publisher_ids</i>
					 - ***Items***
					 - Type: `object`
					 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiespublisher-idsitems">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/publisher/properties/publisher_ids/items</i>
					 - ***Properties***
						 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiespublisher-idsitemspropertiesid">id</b> `required`
							 - ##### ID
							 - *Wert der ID*
							 - Type: `string`
							 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiespublisher-idsitemspropertiesid">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/publisher/properties/publisher_ids/items/properties/id</i>
							 - Length:  &ge; 1

						 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiespublisher-idsitemspropertiestype">type</b> `required`
							 - ##### Typ
							 - *Typ der ID, z.B. gnd. Falls unkbekannt: unknown*
							 - Type: `string`
							 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiespublisherpropertiespublisher-idsitemspropertiestype">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/publisher/properties/publisher_ids/items/properties/type</i>
							 - Example values: 
								 1. *"gnd"*
							 - Length:  &ge; 1

	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesplace">place</b>
		 - #### Erscheinungsort
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesplace">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/place</i>
		 - Length:  &ge; 1

	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesstart-page">start_page</b>
		 - #### Anfangsseite
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesstart-page">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/start_page</i>
		 - Length:  &ge; 1

	 - <b id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesend-page">end_page</b>
		 - #### Endseite
		 - Type: `string`
		 - <i id="httpsuri.gbv.deschemaarticle01schemadefinitionsjournalpropertiesend-page">path: #https://uri.gbv.de/schema/article/01/schema#/definitions/journal/properties/end_page</i>
		 - Length:  &ge; 1


*Generated with [json-schema-md-doc](https://brianwendt.github.io/json-schema-md-doc/)*
*Fri Nov 14 2025 17:52:46 GMT+0100 (Mitteleuropäische Normalzeit)*
