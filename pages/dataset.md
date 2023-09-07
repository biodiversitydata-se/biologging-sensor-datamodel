## Dataset

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
| datasetLicense | string | x |  |  |
** to be finished**

### Contact object
| Field name | Format | Req | Description | Example |
| ---------- | ------ | --- | ----------- | ------- |
| firstName | string | x |  |  |
| lastName | string | x |  |  |
| email | string | x |  |  |
| ORCID | string | x |  |  |

