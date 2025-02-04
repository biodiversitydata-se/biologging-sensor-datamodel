## Dataset

Dataset: A set of data sharing (all or most) properties and that can be described by the same metadata.

Req = Requirement: M = mandatory, R = recommended, O = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| datasetID | string | M |  Unique identifier for a dataset. Recommended format: ... (should be the GBIF dataset DOI) | geolocator_great_snipes_AL | [DwC](https://github.com/biodiversitydata-se/biologging-sensor-datamodel/blob/main/pages/project.md) |
| [projectID](https://github.com/biodiversitydata-se/biologging-sensor-datamodel/blob/main/pages/project.md) | string | M | Unique identifier for a project. | LU_geolocator_great_snipes_AL | . |
| datasetTitle | string | M | A descriptive name for the data set. | Great snipe geolocation by light tracking | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#dataset-resource), [EML](https://sbclter.msi.ucsb.edu/external/InformationManagement/EML_211_schema/docs/eml-2.1.1/eml-resource.html#title) |
| datasetDescription | text | R | A brief overview of the dataset: a descriptive abstract providing enough information to help understand the content of the dataset. <br>Include what (taxon), why (purpose), where (geographic area), when and how (including the sensor system/s chosen).  <br>When data is stored elsewhere include a statement about where the data is stored at and how it is made available. | Migration tracking logger data from Great snipes breeding in Jämtland. | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#dataset-resource), [EML](https://sbclter.msi.ucsb.edu/external/InformationManagement/EML_211_schema/docs/eml-2.1.1/eml-resource.html#abstract) |
| animalCount | integer | O | Number of animals included in the dataset. | 63 | . |
| creator | array of [Contacts](#contact-object) | M | The contact of the creator(-s) for the dataset, i.e. the people who initiated data collection and created this resource. | (see Contact object) |
| contact | array of [Contacts](#contact-object) | M | The contact for the dataset, i.e. the person to be contacted about this resource (who can answerquestions about the dataset in general, or point to others that can). | (see Contact object) |
| curator | array of [Contacts](#contact-object) | O | The contact of the of the curator for the dataset, i.e. the person who is managing the dataset, that is maintaining the data set so it can be accessed and used by people looking for information. | (see Contact object) | [DataCite](https://datacite-metadata-schema.readthedocs.io/en/4.5/appendices/appendix-1/contributorType/#datacurator) |
| owner | array of [Contacts](#contact-object) | M | At least two contacts of the owner for the dataset, i.e. the person(s) possessing the Intellectual Property Rights of the dataset (who can decide about terms of use or grant/deny use of dataset). | (see Contact object) |
| funders | array of [Funders](#funder-object) | O | The list of the different funders with a link to the details of the funding. | (see Funder object) |  |
| license | string | M | The license applied to the dataset, i.e. the legal arrangement specifying what users can do with the data. | CC-BY-NC |
| institutionCode | string | M | The name (or acronym) in use by the institution having ownership of the object(s) or information referred to in the record. | Lund University | [DwC](https://dwc.tdwg.org/terms/#dwc:ownerInstitutionCode) |
| resourceCitation | string | R | Preferred way or default way for how to cite the dataset. | Lindström Å, LastName F, LastName A B (2022). Great snipe geolocation by light tracking. Version 1.X. Lund University. Biologging dataset https://doi.org/10.1xxxxx accessed via yyyyy on 2023-11-30. | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#additional-metadata-natural-collections-description-data-ncd-related) |
| onlineUrl | string | O | URL of dataset (if any). |  | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#dataset-resource) |
| bibliographicCitation | array of [References](#reference-object) | O | One or more DOI's for the citation(-s) of an external resource or additional publication related to or used in the creation of this resource, that serves as an important additional reference for a dataset (e.g. a data paper that describes the dataset, or a paper that is intended to be the canonical or examplar reference to the dataset) (if any). |  | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#additional-metadata-natural-collections-description-data-ncd-related)
| sensorType | array of strings | M | List of sensors with which data were collected in this dataset. See details in the [Sensor object](instrument.md?#sensor-object) |  |
| valuesMeasured | array of strings | M | List of values measured by the different sensors and instruments used in this dataset. | activity, altitude, temperature, pressure | *We need a list here !* |
| unitsReported | array of strings | M | Unit of measurement reported by the different sensors and instruments used in this dataset. Using controlled vocabulary from a predefined list. | degrees C | [https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/unitsReported.md] |
| instrumentTypes | array of strings | M | List of instrument types used in this dataset. | Multi-sensor archival datalogger, GPS Collar | [Biologging standardization](https://github.com/ocean-tracking-network/biologging_standardization/blob/master/templates/fields/instrumentType.md) |
| taxonomicCoverage | array of [Taxon](taxon.md) | M |  | [GBIF metadata profile: taxonomicClassification](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#taxonomic-coverage) (see [Taxon object](taxon.md)) |
| embargoEndDate | date | O | Date when embargo on open access ends (if any). | 2030-01-01 | [DataCite schema: Available](https://schema.datacite.org/meta/kernel-4.4/doc/DataCite-MetadataKernel_v4.4.pdf) |
| accessRights | [enum](#accessRights-enum) | R | Information about whether all of the data is accessible, or only data for certain animals with the remaining data being not public. Restricted access can explain the difference between the numberOfRecords for the dataset and number of records in the downloadable file. Using a controlled [vocabulary](https://github.com/biodiversitydata-se/biologging-sensor-datamodel/blob/main/pages/dataset.md#accessrights) from a predefined list. | see [vocabulary](https://github.com/biodiversitydata-se/biologging-sensor-datamodel/blob/main/pages/dataset.md#accessrights) | [DwC](https://dwc.tdwg.org/terms/#dcterms:accessRights) |
| intellectualRights | string | O | An optional rights management statement for the dataset, for right information regarding usage additional to Copyright covered by the chosen dataset license. Might include requirements for use, requirements for attribution, or other requirements the owner would like to impose. | Free for use by all individuals provided attribution of the original work if this dataset is used, modified and/or distributed in whole or in parts, including acknowledging the owners in any use or publication. | [GBIF Metadata Profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#intellectual-property-rights), [EML](https://eml.ecoinformatics.org/schema/) |
| updateFrequency | string | O | The frequency with which changes are made to the dataset after the initial dataset has been published. Values, e.g.: daily, monthly, weekly, annually, biannually, irregular, asNeeded, notPlanned, unknown. | asNeeded | [EML schema](https://eml.ecoinformatics.org/schema/) |
| geographicCoverage | [GeographicWENS](#geographicwens-object) | M | Spatial information about the dataset. | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#geographic-coverage) (see GeographicWENS object) |
| temporalCoverage| array of RangeDatetime | M | Information about dates or date ranges covered by the resource. Coverages may refer to the times during which the collection or data set was assembled. | (see RangeDatetime object) |
| samplingDescription | string | O | A description of what sampling methods and procedures are or have been used to collect the data represented in the dataset. The description can be augmented by the listing of names or references to methods or sampling procedures. When applicable, specify whether physical measurements (e.g. length, mass, etc.) of organisms were taken. When applicable describe the type(s) of individuals included or excluded when sampling due to developmental stage (e.g. adult, reproductive, larval), and size classes included or excluded (e.g. only small mammals). |  | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#methods) |
| qualityControl | string | O | Information on possible errors or on the quality of a data set: Description of actions taken to either control or assess the quality of data. A quality control description should identify a quality goal and describe prescriptive steps taken to ensure that the data meet those standards and/or postscriptive steps taken to assess the extent to which they are met. Description may refer to instrumentation or software used, and include a reference to a protocol. |  | [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile#methods) |
| relatedIdentifiers | array of [RelatedIdentifier](#relatedIdentifier-object) | O | Identifiers of related resources (e.g. relate to subsets, or a species list, or data at other repository as e.g. Movebank). These must be globally unique identifiers. | 49915781 |  [DataCite](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/relatedidentifier/) |
| versions | array of [Version](#version-object) | O | The historic of the different versions of the resource. Ordered from the most recent one to the older one. |  |
| sensitiveData | boolean | R | Specifies whether data contain protected information, i.e. data contain information that is protected by legislation, e.g. the Species Protection Ordinance. Sensitive data may also apply to information contained in data of records of protected species, disclosure of which may lead to risks for the species. | TRUE |
| pictureUrl | url | R | Url of a picture that can be used for representing the dataset. | |
| isFinalized | boolean | M | Indicates whether the dataset is ongoing or ended. TRUE if the dataset has been ended. | FALSE |
| numberOfRecords | integer | O | Calculated field that stores the number of records in the database for this dataset, public and not public. | 123456789 |
| dateCreated | date | M | The date when the first version of the dataset was published. (date generated at time of publication) |  |
| dateUpdated | date | M | The date when the dataset was last updated. (date generated at time of data update) |  |

### Contact object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| firstName | string | M | The first or given name. | Åke |
| lastName | string | M | The last or family name | Lindström |
| email | string | M | The email address. | ake.lindstrom@biol.lu.se |
| userId | string | O | An identifier that links to a directory of individuals. For example, personal: ORCID Id; organisational: ROR ID | 0000-0002-5597-6209 |
| webpage | url | O | A permanent link to the contact person | |

### Funder object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| funderName | string | R | Name of the funding provider. | Swedish Research Council VR | [DataCite](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/fundingreference/#fundername), [EML](https://eml.ecoinformatics.org/schema/) |
| url | string | O | Link to the webpage of the funding provider. |  |  |

### GeographicWENS object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| westBoundCoordinate | string | M | Western longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 11.9806 |
| eastBoundCoordinate | string | M | Eastern longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 14.345 |
| northBoundCoordinate | string | M | Northern longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 64.090 |
| southBoundCoordinate | string | M | Southern longitudinal dimension of the bounding box. In decimal degrees, with the standard limiting values of -90 to +90 latitude (South/North) and -180 to +180 longitude (West/East). | 61.6859 |
| geographicalDescription | string | O | Textual description of the geographic coverage (geographic scope), i.e. the spatial region or named place where the data was gathered or about which the data is focused. |  |

### RangeDatetime object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| startDatetime | datetime | M | The start date of the time period within which the observations were collected. | 2009-05-21T12:00:00Z | |
| endDatetime | datetime | O | The end date of the time period within which the observations were collected. NULL when data collection is ongoing. | 2021-12-31T12:00:00Z | |

### Reference object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| title | string | M | Title of the reference |  |
| DOI | string | R | DOI of the reference |  |

### RelatedIdentifier object
| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| providerCode | [enum](#providerCode-enum) | M | Code of the provider for the relatedIdentifier |  |
| relationType | [enum](#relationType-enum) | M | Type of relation used from the list. | HasMetadata | [DataCite](https://datacite-metadata-schema.readthedocs.io/en/4.5/appendices/appendix-1/relationType/) |
| identifier | string | M | Unique identifier of related resource (e.g. relate to subsets, or a species list, or data at other repository as e.g. Movebank). | 49915781 |  [DataCite](https://datacite-metadata-schema.readthedocs.io/en/4.5/properties/relatedidentifier/) |
| resourceUrl | url | M | Direct url to the resource. |  |  |


### Version object

List of the different versions of the dataset. Must be ordered from the most recent to the oldest version. 

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| number | string | R | Number of the version. With the format X_Y. X being the major version number, Y the minor version number. | 2.4 | |
| date | string | R | Date of the publication of the version | 2024-04-04 |  |
| log | string | r | Short explanation of the changes done for this version | New data from year XXXX |  |



### Vocabulary

#### accessRights enum

Information about whether all of the data is accessible, or only data for certain animals with the remaining data being not public. Three levels of data access. 
| Value name | Definition |
| ---------- | ------ |
| full open access | All data contained in the dataset are freely accessible by direct download from the website. |
| partial open access | Access to the full dataset is restricted (embargo until YYYY-MM-DD). A sample of records (individual records, or selected events or organisms) is made public by the dataset owner and can be viewed and downloaded from the website. For more information about the full dataset and access please contact the dataset owner. |
| no open access | Access to the full dataset is restricted (embargo until YYYY-MM-DD). No data can be viewed or downloaded from the website. For more information about the dataset and access please contact the dataset owner. |


#### providerCode enum

Information about whether all of the data is accessible, or only data for certain animals with the remaining data being not public. Three levels of data access. 
| Value name | Definition |
| ---------- | ------ |
| Movebank | Dataset coming from Movebank |

#### relationType enum

Information about whether all of the data is accessible, or only data for certain animals with the remaining data being not public. Three levels of data access. 
| Value name | Definition |
| ---------- | ------ |
| Cites |  |
| IsCitedBy |  |
| IsSupplementedBy |  |
| IsSupplementTo |  |
| Describes |  |
| IsDescribedBy |  |
| IsVersionOf |  |
| HasVersion |  |
| IsPartOf |  |
| HasPart |  |
| HasMetadata |  |

