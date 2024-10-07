## Organism

The individual organism (animal) used during event(s) and for which data have been collected in the data set.

Req = Requirement: M = mandatory, R = recommended, O = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| organismID | string | M | Unique identifier for an organism (individual animal). | ..... |
| projectID | string | M | The project this organism has been registered in | LU_geolocator_great_snipes_AL |  |
| datasetID | string | M | The dataset this organism has been registered in | geolocator_great_snipes_AL | |
| isPublic | boolean | M | Indicator of whether the data linked to this organism is public or not. | true |  |
| customProperties | array | M | List of properties for an organism | array("sex" => "female", "age" => "2") | |
| organismTaxon | [Taxon](taxon.md) | M | The taxon info of the organism | (see [Taxon object](taxon.md)) | |


