## Event

Event : An action that occurs at some location during some time, could refer to the deployment of a device or the recording of observations. Event (deployment) information includes information about the organism tagged, tagging protocols followed and tag settings, providing essential information and context for the data collected during the event. May also refer to other event types, for example the handling of the organism.

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| eventID | string | R | Unique identifier for an event (deployment). | 4e72-825a-5fad-2e0d1e901 | [DwC](https://dwc.tdwg.org/terms/#dwc:eventID), [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/deploymentID.md) |
| datasetID | string | R | Identifier of the dataset |  |  |
| organismID | string | R | Unique identifier for an individual, link data from different deployments or instruments on the same organism. |  | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/organismID.md) |
| instrumentID | string | R | Identifier to the instrument |  |  |
| instrumentSettings | array of string | o | Settings used for the instrument during this event. | Sample rate set to every hour |  |
| eventType | string | R | The type of the event (from a list of available values). | handling | [DwC](https://dwc.tdwg.org/terms/#dwc:eventType) |
| eventStartDate | datetime | R | Timestamp the instrument was deployed on the organism. Provides the start of the time period within which the observations were collected. | 2009-05-21T12:00:00Z | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/deploymentDateTime.md) | 
| eventEndDate | datetime | o | Timestamp the instrument was recovered or otherwise detached from the organism (if known). Provides the end of the time period within which the observations were collected. NULL when data collection is ongoing. | 2021-12-31T12:00:00Z | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/detachmentDateTime.md) |
| qualityRemarks | string | r | Comments or notes about the quality of the data recorded for this event. |  |  |
| eventRemarks | string | o | Comments or notes about the event. |  | [DwC](https://dwc.tdwg.org/terms/#dwc:eventRemarks) |
| sensorTypes | array of strings | R | List of type(s) of sensor contained in instrument and used during the event. | Acceleration, Altimeter, Temperature, GeolocationByLight | [biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/sensorType.md)
| eventTaxon | array of Taxon | R |  | (see [Taxon object](dataset.md)) |
| dateCreated | date | R | The date when the first version of the event was published. (date generated at time of publication) |  |
| dateUpdated | date | R | The date when the event was last updated. (date generated at time of data update) |  |
