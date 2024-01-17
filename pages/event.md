## Event

Event: An action that occurs at some location during some time. Within biologging an action can be, for example, the capture of an organims for tagging, the deployment of a device (a collecting or observation equipment), or the recording of observations. Event information includes information relevant to the type of the event, for example, about the organism tagged, tagging protocols followed and tag settings, providing essential information and context for the data collected during the event.

This can be a hierarchy of events, for example a sequence of measurements event has parentEvent deployment. See also [Darwin Core terms for event](https://dwc.tdwg.org/terms/#event) and [GBIF sampling-ecent data - How to capture hierarchy of events?](https://ipt.gbif.org/manual/en/ipt/latest/best-practices-sampling-event-data#how-to-capture-hierarchy-of-events)

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| eventID | string | R | Unique identifier for an event (deployment). | 4e72-825a-5fad-2e0d1e901 | [DwC](https://dwc.tdwg.org/terms/#dwc:eventID), [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/deploymentID.md) |
| datasetID | string | R | Identifier of the dataset |  |  |
| organismID | string | R | Unique identifier for an individual, link data from different deployments or instruments on the same organism. |  | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/organismID.md) |
| instrumentID | string | R | Identifier to the instrument |  |  |
| instrumentSettings | array of string | o | Settings used for the instrument during this event. (flexible format: can be text, key:value pairs, a reference, or URL, DOI)| Sample rate set to every hour |  |
| eventType | string | R | The type of the event. Using a controlled vocabulary, examples include organismCapture, deployment. | deployment | [DwC](https://dwc.tdwg.org/terms/#dwc:eventType) |
| eventStart | datetime | R | Timestamp the instrument was deployed on the organism. Provides the start of the time period within which the observations were collected. | 2009-05-21T12:00:00Z | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/deploymentDateTime.md) | 
| eventEnd | datetime | o | Timestamp the instrument was recovered or otherwise detached from the organism (if known). Provides the end of the time period within which the observations were collected. NULL when data collection is ongoing. | 2021-12-31T12:00:00Z | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/detachmentDateTime.md) |
| qualityRemarks | string | r | Comments or notes about the quality of the data recorded for this event. | "data not recorded due to sensor failure"; "data of poor quality"; "no quality issues" |  |
| eventRemarks | string | o | Comments or notes about the event. |  | [DwC](https://dwc.tdwg.org/terms/#dwc:eventRemarks) |
| sensorTypes | array of strings | R | List of type(s) of sensor contained in instrument and used during the event. | Acceleration, Altimeter, Temperature, GeolocationByLight | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/sensorType.md)
| eventTaxon | array of Taxon | R |  | (see [Taxon object](dataset.md)) |
| dateCreated | date | R | The date when the first version of the event was published. (date generated at time of publication) |  |
| dateUpdated | date | R | The date when the event was last updated. (date generated at time of data update) |  |


### Vocabulary

#### eventType
| Value name | Definition |
| ---------- | ------ |
| organismCapture |  |
| deployment | the action of a device (collecting or observation equipment) collecting observations |
|  |  |
|  |  |
