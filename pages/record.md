## Record

.... 

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| recordID | string | R | Unique identifier for a record | | |
| sensorID | string | R | Identifier of the sensor that recorded the data |  | |
| eventID | string | R | Identifier of the event |  | |
| datasetID | string | R | Identifier of the dataset |  | |
| recordTime | datetime | R | The recording date and time | 2009-05-21T12:00:00Z | |
| recordValues | array of keyValue | R | Array containing all the values mesured for this record. THe key must be in the same order as in the instrument.sensor.valuesMeasured | |
| dateCreated | date | R | The date when the first version of the record was published. (date generated at time of publication) |  |
| dateUpdated | date | R | The date when the record was last updated. (date generated at time of data update) |  |


### KeyValue object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| key | string | R | Identifier of the key | | |
| value | string | R | Value measured | | |