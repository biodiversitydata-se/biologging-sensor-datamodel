## Dataset

Dataset: A set of data sharing (all or most) properties and that can be described by the same metadata.

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| datasetID | string | R |  Unique identifier for a dataset. Recommended format: ... (should be the GBIF dataset DOI) | geolocator_great_snipes_AL |
| [projectID](pages/project.md) | string | R | Unique identifier for a project. | LU_geolocator_great_snipes_AL |
| datasetTitle | string | R | A descriptive name for the data set. | Great snipe geolocation by light tracking |
| datasetDescription | text | r | A brief overview of the dataset: a descriptive abstract providing enough information to help understand the content of the dataset. <br>Include what (taxon), why (purpose), where (geographic area), when and how (including the sensor system/s chosen). | Migration tracking logger data from Great snipes breeding in Jämtland. |
| animalCount | integer | o | Number of animals included in the dataset. | 63 |
| creator | array of contacts | R | The contact of the creator(-s) for the dataset, i.e. the people who initiated data collection and created this resource. | (see Contact object) |
| contact | array of contacts | R | The contact for the dataset, i.e. the person to be contacted about this resource (who can answerquestions about the dataset in general, or point to others that can). | (see Contact object) |
| curator | array of contacts | o | The contact of the of the curator for the dataset, i.e. the person who is managing the dataset, that is maintaining the data set so it can be accessed and used by people looking for information. | (see Contact object) |
| owner | array of contacts | R | At least two contacts of the owner for the dataset, i.e. the person(s) possessing the Intellectual Property Rights of the dataset (who can decide about terms of use or grant/deny use of dataset). | (see Contact object) |
| license | string | R | The license applied to the dataset, i.e. the legal arrangement specifying what users can do with the data. | CC-BY-NC |
| institutionCode | string | R | The name (or acronym) in use by the institution having ownership of the object(s) or information referred to in the record. | Lund University | https://dwc.tdwg.org/terms/#dwc:ownerInstitutionCode |
| resourceCitation | string | r | Preferred way or default way for how to cite the dataset. | Lindström Å, LastName F, LastName A B (2022). Great snipe geolocation by light tracking. Version 1.X. Lund University. Biologging dataset https://doi.org/10.1xxxxx accessed via yyyyy on 2023-11-30. |
| onlineUrl | string | o | URL of dataset (if any). |  |
| bibliographicCitation | array of references | o | One or more DOI's for the citation(-s) of an external resource or additional publication related to or used in the creation of this resource, that serves as an important additional reference for a dataset (e.g. a data paper that describes the dataset, or a paper that is intended to be the canonical or examplar reference to the dataset) (if any). |  |
| sensorTypes | array of strings | R | List of sensor types used in this dataset. | Acceleration, Altimeter, Temperature, GeolocationByLight |
| instrumentTypes | array of strings | R | List of instrument types used in this dataset. | Multi-sensor archival datalogger, GPS Collar |
| taxonomicCoverage | array of Taxon | R |  | (see Taxon object) |
| embargoEndDate | date | o | Date when embargo on open access ends (if any). | 2030-01-01 |
| isPublic | boolean | o | Indicator of whether the dataset is free to use. | true |
| updateFrequency | string | o | The frequency with which changes are made to the dataset after the initial dataset has been published. Values, e.g.: daily, monthly, weekly, annually, biannually, irregular, asNeeded, unknown. | asNeeded |
| geographicCoverage | GeographicWENS | R | Spatial information about the dataset. | (see GeographicWENS object) |
| temporalCoverage| array of RangeDatetime | R | Information about dates or date ranges covered by the resource. Coverages may refer to the times during which the collection or data set was assembled. | (see RangeDatetime object) |
| samplingDescription | string | o | A description of what sampling methods and procedures are or have been used to collect the data represented in the dataset. The description can be augmented by the listing of names or references to methods or sampling procedures. When applicable, specify whether physical measurements (e.g. length, mass, etc.) of organisms were taken. When applicable describe the type(s) of individuals included or excluded when sampling due to developmental stage (e.g. adult, reproductive, larval), and size classes included or excluded (e.g. only small mammals). |  |
| qualityControl | string | o | Information on possible errors or on the quality of a data set: Description of actions taken to either control or assess the quality of data. A quality control description should identify a quality goal and describe prescriptive steps taken to ensure that the data meet those standards and/or postscriptive steps taken to assess the extent to which they are met. Description may refer to instrumentation or software used, and include a reference to a protocol. |  |
| relatedIdentifier | string | o | Identifiers of related resources (e.g. relate to subsets, or a species list). These must be globally unique identifiers. |  |
| relationType | string | o | If RelatedIdentifier is used, relationType is mandatory. Use from vocabulary: Cites, IsCitedBy, IsSupplementedBy, IsSupplementTo, Describes, IsDescribedBy, IsVersionOf, HasVersion, IsPartOf, HasPart. |  |
| version | string | o | The version number of the resource. Suggested practice: track major_version.minor_version. Register a new identifier for a major version change. |  |
| sensitiveData | boolean | r | Specifies whether data contain protected information, i.e. data contain information that is protected by legislation, e.g. the Species Protection Ordinance. Sensitive data may also apply to information contained in data of records of protected species, disclosure of which may lead to risks for the species. | TRUE |
| dateCreated | date | R | The date when the first version of the dataset was published. (date generated at time of publication) |  |
| dateUpdated | date | R | The date when the dataset was last updated. (date generated at time of data update) |  |

### Contact object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| firstName | string | R | The first or given name. | Åke |
| lastName | string | R | The last or family name | Lindström |
| emailAddress | string | R | The email address. | ake.lindstrom@biol.lu.se |
| userId | string | o | An identifier that links to a directory of individuals. For example, personal: ORCID Id; organisational: ROR ID | 0000-0002-5597-6209 |

### Taxon object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| guid | string | r | Id of a taxon covered by the dataset. | urn:lsid:dyntaxa.se:Taxon:100061 |
| scientificName | string | R |  | Gallinago media |
| commonName | string | o |  | Great snipe |

### GeographicWENS object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| westBoundCoordinate | string | R | Western longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 11.9806 |
| eastBoundCoordinate | string | R | Eastern longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 14.345 |
| northBoundCoordinate | string | R | Northern longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 64.090 |
| southBoundCoordinate | string | R | Southern longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 61.6859 |
| geographicalDescription | string | o | Textual description of the geographic coverage (geographic scope), i.e. the spatial region or named place where the data was gathered or about which the data is focused. |  |

### RangeDatetime object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| startDatetime | datetime | R | The start date of the time period within which the observations were collected. | 2009-05-21T12:00:00Z | |
| endDatetime | datetime | o | The end date of the time period within which the observations were collected. NULL when data collection is ongoing. | 2021-12-31T12:00:00Z | |

### Reference object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| DOI | string | r | DOI |  |  |
| url | string | o | Url |  |  |
| Definition | string | o | Url |  |  |
