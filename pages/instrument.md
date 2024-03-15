## Instrument

The instrument metadata contain all information pertaining to the biologging instrument used to collect data in the dataset. Instrument specifications encompass also specifications for the included sensors, i.e. the device sensitive to light, temperature, radiation level, or the like, and that transmits a signal. Here we use instrument synonymous for device or tag.

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| instrumentID |  | R | Unique identifier of the instrument. Can be the instrument serial number, or other similar identification system used by the manufacturer. |  | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentID.md] |
| projectID | string | R | The project this instrument belongs to | LU_geolocator_great_snipes_AL |
| instrumentType | enum | R | Type of instrument deployed (from a predefined list). | GPS Collar | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentType.md] |
| instrumentModel | string | R | Name of specific instrument model deployed. |  | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentModel.md] |
| instrumentManufacturer | string | R | Manufacturer of the instrument. | Vectronic Aerospace | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentManufacturer.md] |
| instrumentSerialNumber | string | R | Serial number of instrument deployed. | 09A0178 | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentSerialNumber.md] |
| instrumentCharacteristics | array | R | List of characteristics for an instrument | array("wavelength" => "X-band", "power" => "200 kW", "pulseDuration" => "0.25 microseconds", "pulseRepetition" => "504 Hz", "beamWidth" => "1.5 deg (-3db)") |
| sensors | array of sensors | R | Specifications for the sensors included in the instrument. | (see sensor object) |


### Sensor object


| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| sensorID | string | R | Unique identifier of the sensor. |  |
| sensorType | string | R |  |  |
| sensorManufacturer | string | R |  |  |
| valuesMeasured | array of strings | R | Attribute names of the values measured, as it will be mentionned in the record.recordValues.key |  |
| unitsReported | array of strings | R | Unit of measurement reported. | degrees C | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/unitsReported.md] |
| sensorPrecision | string | r |  |  |
| range | string | r |  |  |
| settings | string | o |  |  |
| calibrationDate | string | r |  |  |
| calibrationDetails | string | r |  |  |


### Vocabulary

#### instrumentType
| Value name | Definition |
| ---------- | ------ |
| GPStag | device (tag) containing a GPS sensor, can be a collar, backpack or other. |
| geolocator |  (tag) that containing a sensor that records records ambient light level to determine location. may contain additional sensors. |
| PIT | Passive Integrated Transponder |
| radar |  |
|  |  |
|  |  |
|  |  |

#### sensorType
| Value name | Definition |
| ---------- | ------ |
| accelerometer |  |
| GPS |  |
| thermometer |  |
| pressureGauge |  |
|  |  |
|  |  |
