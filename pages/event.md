## Event

.... deployment

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| eventID | string | R | Unique identifier for an event. | |  |
| datasetID | string | R | Identifier of the dataset | |  |
| organismID | string | R | Identifier of the organism | |  |
| instrumentID | string | R | Identifier to the instrument | |  |
| instrumentIDSource | string | ? | ??? | |  |
| instrumentSetupDetails | array of string | ? | ??? | |  |
| eventStartDate | datetime | R | The start date of the time period within which the observations were collected. | 2009-05-21T12:00:00Z | | 
| eventEndDate | datetime | o | The end date of the time period within which the observations were collected. NULL when data collection is ongoing. | 2021-12-31T12:00:00Z | |
| eventDetails | string | ? | ??? | |  |
| sensorTypes | array of strings | R | List of sensor types used in this dataset. | Acceleration, Altimeter, Temperature, GeolocationByLight |
| eventTaxon | array of Taxon | R |  | (see [Taxon object](dataset.md)) |
| dateCreated | date | R | The date when the first version of the event was published. (date generated at time of publication) |  |
| dateUpdated | date | R | The date when the event was last updated. (date generated at time of data update) |  |
