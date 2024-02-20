## Taxon object

Taxon: Species item identified by its guid coming from the [SBDI species module](species.biodiversitydata.se), and its dyntaxaId from [artfakta.se]

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| taxonListSourceUrl | string | R | Link to the species list where the item comes from. SBDI module species.biodiversitydata.se  | https://collections.biodiversitydata.se/public/show/7ddf754f-d193-4cc9-b351-99906754a03b | [Species API](https://species.biodiversitydata.se/ws/openapi#/Search)
| taxonListSourceName | string | R | Name of the species where the item comes from. | "GBIF Backbone Taxonomy" |
| taxonGuid | string | R | Id of the species in the SBDI species module | 2481831 |
| taxonScientificName | string | R | ScientificName of the species | Great snipe |
| taxonCommonName | string | R | Common name displayed | Great snipe |
| dyntaxaId | string | R | DyntaxaId of the species as specified in artfakta.se | 100061 |
