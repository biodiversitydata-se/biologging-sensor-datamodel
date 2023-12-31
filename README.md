# biologging-datamodel
Data model documentation - describes the components (objects) of the data model and their properties. The data objects are described by a data dictionary, listing each objects’s properties (fields), with their name and a description. 
A Data Dictionary is a collection of names, definitions, and attributes about data objects that are being used or captured in a database, information system, or part of a research project.

## Data model used in the [SBDI biologging API](https://github.com/biodiversitydata-se/sensorprojectAPI) and client

### Objects

 - [Project](pages/project.md)
 - [Dataset](pages/dataset.md)
 - [Deployment / Event](pages/event.md)
 - [Record](pages/record.md)
 - [Instrument](pages/instrument.md) / Device
 - Organism

### Data model

PICTURE. illustration of data model. placeholder

Description of data model: A project comprises one or more datasets. Each dataset contains a core of events (deployments) defining the location and duration of an event and additional event properties. The event core is extended by information about the organism that is acting during the event, one or more instruments used during the event, one or more sensors used during the event, extended measurements or facts linked to the event (deployment), and the data records collected during the event.

Basis for this work on [A standardisation framework for bio-logging data](https://github.com/ocean-tracking-network/biologging_standardization/tree/master), published Sequeira et al. 2021 A standardisation framework for bio-logging data to advance ecological research and conservation. Methods in Ecology and Evolution 12, 996-1007  [https://doi.org/10.1111/2041-210X.13593]( https://doi.org/10.1111/2041-210X.13593).

* this repo is now linked to our Slack channel