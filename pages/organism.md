## Organism

The individual organism (animal) used during event(s) and for which data have been collected in the data set.

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| organismID | string | R | Unique identifier for an organism (individual animal). | ..... |
| projectID | string | R | The project this organism has been registered in | LU_geolocator_great_snipes_AL |
| datasetID | string | R | The dataset this organism has been registered in | geolocator_great_snipes_AL |
| customProperties | array | R | List of properties for an organism | array("sex" => "female", "age" => "2") |
| organismTaxon | [Taxon](taxon.md) | R | The taxon info of the organism | (see [Taxon object](taxon.md)) |


