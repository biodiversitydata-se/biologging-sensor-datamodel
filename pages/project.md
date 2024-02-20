## Project

A (research) project providing the context under which the data in the dataset were produced.

Req = requirement: R = required, r = recommended, o = optional.

| Field name | Format | Req | Definition | Example | Reference |
| ---------- | ------ | --- | ---------- | ------- | --------- |
| projectID | string | R | Unique identifier for a project. | LU_geolocator_great_snipes_AL |
| projectName | string | R | A descriptive name for the project. | Geolocator Great snipes Jämtland ÅL |
| projectDescription | text | r | A brief overview of the project: a descriptive abstract providing enough information to help understand <br>the purpose of the project, and the datasets it contains. Include what, why, where, when and how. | ... |
| projectCreatedDate | date | r | Project start date/timestamp | 2009-05-15 |
| projectUpdatedDate | date | r | Project last updated date/timestamp | 2023-08-21 |
| isFinalized | boolean | R | Indicates whether the project is ongoing or ended. TRUE if the project has been ended. | FALSE |
| createdDate | string | r | The date when project metadata was created. | 2009-11-29 |
| updatedDate | string | r | The date when project metadata was updated. | 2022-11-01 |

<br>
Note - To be investigated: <br> Project may be defined at a level above dataset (i.e. a project under which data in one or more datasets were produced) and also (?) at a level below dataset (i.e. delimit data parts that were produced, for example, 
in a specific area, population and/or time period).
