## Project

A (research) project providing the context under which the data in the dataset were produced.

Req = Requirement: M = mandatory, R = recommended, O = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| projectID | string | M | Unique identifier for a project. | LU_geolocator_great_snipes_AL |
| projectName | string | M | A descriptive name for the project. | Geolocator Great snipes Jämtland ÅL |
| projectDescription | text | R | A brief overview of the project: a descriptive abstract providing enough information to help understand <br>the purpose of the project, and the datasets it contains. Include what, why, where, when and how. | ... |
| projectCreatedDate | date | R | Project start date/timestamp | 2009-05-15 |
| projectUpdatedDate | date | R | Project last updated date/timestamp | 2023-08-21 |
| isFinalized | boolean | M | Indicates whether the project is ongoing or ended. TRUE if the project has been ended. | FALSE |
| createdDate | string | R | The date when project metadata was created. | 2009-11-29 |
| updatedDate | string | R | The date when project metadata was updated. | 2022-11-01 |

<br>
Note - To be investigated: <br> Project may be defined at a level above dataset (i.e. a project under which data in one or more datasets were produced) and also (?) at a level below dataset (i.e. delimit data parts that were produced, for example, 
in a specific area, population and/or time period).
