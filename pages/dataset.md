## Dataset

kkkahhaf

Req = required. If nothing indicated : optional

| Field name | Format | Req | Description | Example |
| ---------- | ------ | --- | ----------- | ------- |
| datasetID | string | x |  | Unique identifier for a dataset. Recommended format: ... (should be the GBIF dataset DOI) |
| [projectID](pages/project.md) | string | x | Unique identifier for a project. Recommended format: ... |  |
| datasetName | string | x | A descriptive name for the data set. |  |
| datasetDescription | text | x | A brief overview of the dataset: a descriptive abstract providing enough information to help understand the content of the dataset. Include what (taxon), why (purpose), where (geographic area), when and how (including the sensor system/s chosen). |  |
| animalCount | integer |  | Number of animals included in dataset |  |
| contactCreators | array of contacts | x | The contact of the creators (who initiated data collection) for the dataset or project. |  |
| contactQuestions | contact |  | The contact of the person who can answer questions about the dataset in general, or point to others that can |  |
| contactCuratorOwner | array of contacts |  | The contact of the person who can decide about terms of use or grant/deny use of dataset |  |
| datasetLicense | string | x | Enum of specific licence type | CC-BY-NC |
| datasetOwner | Contact | x |  | Who owns the Intellectual Property Rights of the dataset). |
| datasetCitation | string |  | Preferred way or default way for how to cite the dataset. |  |
| datasetReferences | array of strings |  | List of DOI for the dataset |  |
| sensorTypes | array of strings | x | List of sensor types used in this dataset. | Acceleration, Altimeter, Temperature, GeolocationByLight |
| datasetTaxon | array of Taxons | x |  |  |
| embargoEndDate | date |  | Date when embargo on open access ends (if any) | 2030-01-01 |
| isPublic | boolean |  | Indicator of whether the dataset is free to use. | true |
| updateFrequency | string |  |  | The frequency with which changes are made to the dataset after the initial dataset has been published. Values, e.g.: daily, monthly, unknown, three times per month, three times per year, every other month, weekly, yearly, other. |
| geographicalCoverage | GeographicWENS |  |  |  |
| startDate | datetime | x | The start date of the time period within which the observations were collected. | 2009-05-21T12:00:00Z |
| endDate | datetime |  | The end date of the time period within which the observations were collected. NULL when data collection is ongoing. | 2021-12-31T12:00:00Z |
| samplingDescription | string |  | A description of what sampling methods and procedures are or have been used in the research project. The description can be augmented by the listing of names or references to methods or sampling procedures using the field samplingMethods. When applicable, specify whether physical measurements (e.g. length, mass, etc.) of organisms were taken. When applicable describe the type(s) of individuals included or excluded when sampling due to developmental stage (e.g. adult, reproductive, larval), and size classes included or excluded (e.g. only small mammals). |  |
| qualityControl | string |  | Information on possible errors or on the quality of a data set: Description of actions taken to either control or assess the quality of data. A quality control description should identify a quality goal and describe prescriptive steps taken to ensure that the data meet those standards and/or postscriptive steps taken to assess the extent to which they are met. Description may refer to instrumentation or software used, and include a reference to a protocol. |  |
| relatedIdentifier | string |  | Identifiers of related resources (e.g relate to subsets, or a species list). These must be globally unique identifiers. |  |
| relationType | string |  | If RelatedIdentifier is used, relationType is mandatory. Use from vocabulary: Cites, IsCitedBy, IsSupplementedBy, IsSupplementTo, Describes, IsDescribedBy, IsVersionOf, HasVersion, IsPartOf, HasPart. |  |
| version | string |  | The version number of the resource. Suggested practice: track major_version.minor_version. Register a new identifier for a major version change. |  |
| sensitiveData | string |  | Specifies whether data contain protected information, i.e. data contain information that is protected by legislation, e.g. the Species Protection Ordinance. Sensitive data may also apply to information contained in data of records of protected species, disclosure of which may lead to risks for the species. |  |


| dateCreated | date | x | The date when the first version of the dataset was published. (date generated at time of publication) |  |
| dateUpdated | date | x | The date when the dataset was updated. (date generated at time of data update) |  |
** to be finished**

### Contact object
| Field name | Format | Req | Description | Example |
| ---------- | ------ | --- | ----------- | ------- |
| firstName | string | x |  | Åke |
| lastName | string | x |  | Lindström |
| email | string | x |  | ake.lindstrom@biol.lu.se |
| ORCID | string | x |  | 0000-0002-5597-6209 |

### Taxon object
| Field name | Format | Req | Description | Example |
| ---------- | ------ | --- | ----------- | ------- |
| guid | string | x | Id of the species item | urn:lsid:dyntaxa.se:Taxon:100061 |
| scientificName | string | x |  | Gallinago media |
| commonName | string | x |  | Great snipe |


### GeographicWENS object
| Field name | Format | Req | Description | Example |
| ---------- | ------ | --- | ----------- | ------- |
| westBoundCoordinate | string |  | Western longitudinal dimension of the bounding box. In decimal degrees (e.g. 17.6577), with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). |  |
| eastBoundCoordinate | string |  |  |  |
| northBoundCoordinate | string |  |  |  |
| southBoundCoordinate | string |  |  |  |
| geographicalDescription | string |  | Textual description of the geographic coverage (geographic scope), i.e. the spatial region or named place where the data was gathered or about which the data is focused. |  |
