## Taxon object

Taxon: Species item identified by its guid coming from the [SBDI species module](species.biodiversitydata.se), and its dyntaxaId from [artfakta.se]

Req = Requirement: M = mandatory, R = recommended, O = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| taxonListSourceUrl | string | M | Link to the species list where the item comes from. SBDI module species.biodiversitydata.se  | https://collections.biodiversitydata.se/public/show/7ddf754f-d193-4cc9-b351-99906754a03b | [Species API](https://species.biodiversitydata.se/ws/openapi#/Search)
| taxonListSourceName | string | M | Name of the species where the item comes from. | "GBIF Backbone Taxonomy" |
| taxonGuid | string | M | Id of the species in the SBDI species module | 2481831 |
| taxonScientificName | string | M | ScientificName of the species | Gallinago media |
| taxonCommonName | string | M | Common name displayed | Great snipe |
| dyntaxaId | string | M | DyntaxaId of the species as specified in artfakta.se | 100061 |
