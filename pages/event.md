## Event

Event: An action that occurs at some location during some time. Within biologging an action can be, for example, the capture of an organims for tagging, the deployment of a device (a collecting or observation equipment), or the recording of observations. Event information includes information relevant to the type of the event, for example, about the organism tagged, tagging protocols followed and tag settings, providing essential information and context for the data collected during the event.

This can be a hierarchy of events, for example a sequence of measurements events has parentEvent deployment. See also [Darwin Core terms for event](https://dwc.tdwg.org/terms/#event) and [GBIF sampling-ecent data - How to capture hierarchy of events?](https://ipt.gbif.org/manual/en/ipt/latest/best-practices-sampling-event-data#how-to-capture-hierarchy-of-events)

Requirement: M = mandatory, R = recommended, O = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| eventID | string | M | Unique identifier for an event (deployment). | 4e72-825a-5fad-2e0d1e901 | [DwC](https://dwc.tdwg.org/terms/#dwc:eventID), [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/deploymentID.md) |
| datasetID | string | M | Identifier of the dataset |  |  |
| organismID | string | M | Unique identifier for an individual, link data from different deployments or instruments on the same organism. |  | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/organismID.md) |
| instrumentID | string | M | Identifier to the instrument. |  |  |
| instrumentSettings | array of string | O | Settings used for the instrument during this event. (flexible format: can be text, key:value pairs, a reference, or URL, DOI)| Sample rate set to every hour |  |
| eventType | string | M | The type of the event. Using a controlled [vocabulary](https://github.com/biodiversitydata-se/biologging-sensor-datamodel/blob/main/pages/event.md#eventtype), examples include organismCapture, deployment. | deployment | [DwC](https://dwc.tdwg.org/terms/#dwc:eventType) |
| eventStart | datetime | M | Timestamp for the start of the event. Provides the start of the time period within which the observations were collected. | 2009-05-21T12:00:00Z | [DwC](https://dwc.tdwg.org/terms/#dwc:eventTime), [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/deploymentDateTime.md) | 
| eventEnd | datetime | O | Timestamp for the end of the event. Provides the end of the time period within which the observations were collected. NULL when data collection is ongoing. | 2021-12-31T12:00:00Z | [DwC](https://dwc.tdwg.org/terms/#dwc:eventTime), [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/detachmentDateTime.md) |
| qualityRemarks | string | R | Comments or notes about the quality of the data recorded for this event. | "data not recorded due to sensor failure"; "data of poor quality"; "no quality issues" |  |
| eventRemarks | string | O | Comments or notes about the event. |  | [DwC](https://dwc.tdwg.org/terms/#dwc:eventRemarks) |
| valuesMeasured | array of strings | M | List of values measured by the different sensors and instruments used in this event. | activity, altitude, temperature, pressure | *We need a list here !* |
| eventTaxon | array of [Taxon](taxon.md) | M |  | (see [Taxon object](taxon.md)) |
| organismPublic | string | M | Ineherited field that tells if the data from the animal recorded can be published (based on isPublic field in [Organism](organism.md) object) | true | |
| numberOfRecords | integer | O | Calculated field that stores the number of records in the database for this event, public and not public. | 123456789 |
| dateCreated | date | M | The date when the first version of the event was published. (date generated at time of publication) |  |
| dateUpdated | date | M | The date when the event was last updated. (date generated at time of data update) |  |


### Vocabulary

#### eventType
| Value name | Definition |
| ---------- | ------ |
| organismCapture | During a capture event an organism is captured and released, typically for the purpose of attaching an instrument (tag). Measurements may be taken that describe the state of the organism or external conditions at the capture event. |
| deployment | A deployment event spans the period of time a sensor is functioning properly in the field on a particular organism or at a particular location, and may follow a specified protocol. For example, instruments (tags) deployed on a moving organism, or instruments (e.g. radar) installed at a location (e.g. radar station). |
| tracking | A tracking event is started after the deployment of an instrument on an organism (e.g. continous recording of scheduled recordings of positions or body temperature),  or is triggered by an instrument deployed on an organism when a signal is received by a receiver instrument at a specified location (e.g. PIT tags), or is triggered at the same location as the deployment covering the field of view of the instrument (e.g. radar). Each tracking event spans a specific time period defining the bounds of the event. Each tracking event consists of one or more records of values measured by the sensor. |
| deployOff | During a deployment-off event the animal is recaptured and/or the tag retrieved, ending the deployment. |
