## Instrument

The instrument metadata contain all information pertaining to the biologging instrument used to collect data in the dataset. Instrument specifications encompass also specifications for the included sensors, i.e. the device sensitive to light, temperature, radiation level, or the like, and that transmits a signal. Here we use instrument synonymous for device or tag.

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| instrumentID |  | R | Unique instrument ID. Can be the instrument serial number, or other similar identification system used by the manufacturer. |  | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentID.md] |
| instrumentType | enum | R | Type of instrument deployed (from a predefined list). | GPS Collar | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentType.md] |
| instrumentModel | string | R | Name of specific instrument model deployed. |  | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentModel.md] |
| instrumentManufacturer | string | R | Manufacturer of the instrument. | Vectronic Aerospace | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentManufacturer.md] |
| instrumentSerialNumber | string | R | Serial number of instrument deployed. | 09A0178 | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentSerialNumber.md] |
| instrumentCharacteristics | array | R |  | example of tracking radar instrument: instrumentCharacteristics = array("wavelength" => "X-band", "power" => "200 kW", "pulseDuration" => "0.25 microseconds", "pulseRepetition" => "504 Hz", "beamWidth" => "1.5 deg (-3db)") |
| sensors | array of sensors | R | Specifications for the sensors included in the instrument. | (see sensor object) |


### Sensor object


| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| sensorID | string | R |  |  |
| sensorType | string | R |  |  |
| sensorManufacturer | string | R |  |  |
| valuesMeasured | string | R | Attribute name of the values measured, as it will be mentionned in the record.recordValues.key |  |
| unitsReported | string | R | Unit of measurement reported. | degrees C | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/unitsReported.md] |
| sensorPrecision | string | R |  |  |
| range | string | R |  |  |
| settings | string | o |  |  |
| calibrationDate | string | r |  |  |
| calibrationDetails | string | r |  |  |
