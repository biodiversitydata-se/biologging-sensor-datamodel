## Dataset

Req = required. If nothing indicated : optional

| Field name | Format | Req | Description | Example |
| ---------- | ------ | --- | ----------- | ------- |
| instrumentType | enum | x | Type of instrument among a predefined list | GPS Collar |
| instrumentModel | string | x | Name of the model of the instrument |  |
| instrumentManufacturer | string | x | Manufacturer of the instrument | |
| instrumentSerialNumber | string | x | Serial number of the instrument |  |
| instrumentCharacteristics | array | x | Project last updated date/timestamp |  |
| sensors | array | x |  |  |


### Sensor object


| Field name | Format | Req | Description | Example |
| ---------- | ------ | --- | ----------- | ------- |
| sensorID | string | x |  |  |
| sensorType | string | x |  |  |
| valuesMeasured | string | x |  |  |
| unitsReported | string | x |  |  |
| sensorPrecision | string | x |  |  |
| range | string | x |  |  |
| settings | string | x |  |  |
