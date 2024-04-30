## Instrument

The instrument metadata contain all information pertaining to the biologging instrument used to collect data in the dataset. Instrument specifications encompass also specifications for the included sensors, i.e. the device sensitive to light, temperature, radiation level, or the like, and that transmits a signal. Here we use instrument synonymous for device or tag.

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| instrumentID |  | R | Unique identifier of the instrument. Can be the instrument serial number, or other similar identification system used by the manufacturer. |  | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentID.md] |
| projectID | string | R | The project this instrument belongs to. | LU_geolocator_great_snipes_AL |
| instrumentType | enum | R | Type of instrument. Using controlled vocabulary from a predefined list. | GPS Collar | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentType.md] |
| instrumentModel | string | R | Name of specific instrument model deployed. |  | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentModel.md] |
| instrumentManufacturer | string | R |  The company or person that produced the instrument. | Vectronic Aerospace | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentManufacturer.md] |
| instrumentSerialNumber | string | R | Serial number of the instrument. | 09A0178 | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentSerialNumber.md] |
| instrumentCharacteristics | array | R | List of characteristics for an instrument | array("wavelength" => "X-band", "power" => "200 kW", "pulseDuration" => "0.25 microseconds", "pulseRepetition" => "504 Hz", "beamWidth" => "1.5 deg (-3db)") |
| sensors | array of sensors | R | Specifications for the sensors included in the instrument. | (see [Sensor object](#sensor-object)) |


### Sensor object


| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| sensorID | string | R | Unique identifier of the sensor. |  |
| sensorType | string | R | The type of sensor with which data were collected. All sensors are associated with an instrument (tag) id, and instrument can contain multiple sensor types. Each event record is assigned one sensor type. Using controlled vocabulary from a predefined list. |  |
| sensorManufacturer | string | R | The company or person that produced the sensor. |  |
| valuesMeasured | array of strings | R | Attribute names of the values measured, as it will be mentioned in the record.recordValues.key Using controlled vocabulary from a predefined list. |  |
| unitsReported | array of strings | R | Unit of measurement reported. Using controlled vocabulary from a predefined list. | degrees C | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/unitsReported.md] |
| sensorPrecision | string | r |  |  |
| range | string | r |  |  |
| settings | string | o |  |  |
| calibrationDate | string | r |  |  |
| calibrationDetails | string | r |  |  |


### Vocabulary

#### instrumentType
| Value name | Definition |
| ---------- | ------ |
| gpsTag | Device (tag) containing a GPS sensor, can be a collar, backpack or other. |
| geolocator |  Device (tag) containing a sensor that records ambient light level to determine location. May contain additional sensors. |
| PIT | Passive Integrated Transponder, or PIT tag, an internal tag containing a microchip that is activated when it passes close to a scanning device, sending a unique alpha-numeric code back to the reader. (Gibbons WJ & Andrews KM 2004. PIT Tagging: Simple Technology at Its Best. BioScience 54, 447–454, [DOI](https://doi.org/10.1641/0006-3568(2004)054[0447:PTSTAI]2.0.CO;2)) |
| radar | Detection radar (radar: acronym for radio detection and ranging). A stationed radar unit (antenna) emits pulses of electromagnetic radiation with the beam of pulsed energy moving away from the radar. When something interferes with the beam some of the energy of the initial pulse is scattered and some of the energy from these pulses is reflected back to the radar antenna. The radar provides information the magnitude, extent, distance and location, and speed of the targets detected on radar. (Bruderer B 1997. The Study of Bird Migration by Radar Part 1: The Technical Basis. Naturwissenschaften 84, 1–8, [DOI](https://doi.org/10.1007/s001140050338). Bruderer B 1997. The Study of Bird Migration by Radar Part 2: Major Achievements. Naturwissenschaften 84, 45–54, [DOI](https://doi.org/10.1007/s001140050348)) |
| tempTag | non-spatial, measures core temperature in the animal. (in WRAM called DST, although DST simply stands for Data Storage Tag) |
| activityTag | non-spatial, measures heart rate and activity rates. (in WRAM called RVL (Reveal)) |
| mortalityTag | non-spatial, mortality implant, measures body temperature, heart rate and sends mortality message. (in WRAM called MTI) |
| (type) |  |

#### sensorType
| Value name | Definition |
| ---------- | ------ |
| accelerometer |  |
| GPS |  |
| thermometer |  |
| pressureGauge |  |
| (type) |  |
| (type) |  |

#### valuesMeasured
| Value name | Definition |
| ---------- | ------ |
| tempearature |  |
| (value) |  |

#### unitsReported
| Value name | Definition |
| ---------- | ------ |
| degrees C |  |
| (value) |  |
