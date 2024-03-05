# biologging-datamodel
Biologging data is data collected from wild animals employing animal-attached electronic tags to uncover the hidden lives of wild animals. In the simplest case, the data is a time-series of positions, recording the movement of animals. Other more sophisticated sensor systems attached to the animals can collect information on the physiological status of the animal (heart rate, temperature, etc.), behaviour patterns (e.g. activity level or flight altitude) and other parameters of interest. Data is collected by tags (syn. with instrument, device) including sensors and retrieved or remotely transmitted, or collected from radar/optical sensors that target animals. 

This data model documentation describes the components (objects) of the data model and their properties. The data objects are described by a data dictionary, listing each objects’s properties (fields), with their name and a description. 
A Data Dictionary is a collection of names, definitions, and attributes about data objects that are being used or captured in a database, information system, or part of a research project.

## Data model used in the [SBDI biologging API](https://github.com/biodiversitydata-se/sensorprojectAPI) and client

### Objects

 - [Project](pages/project.md)
 - [Dataset](pages/dataset.md)
 - [Event](pages/event.md)
 - [Record](pages/record.md)
 - [Instrument](pages/instrument.md) (including the Sensor object)
 - [Taxon](pages/taxon.md)
 - [Organism](pages/organism.md)

### Data model

PICTURE - placeholder. illustration of data model

Description of data model: A project comprises one or more datasets. Each dataset contains a core of events (deployments) defining the location and duration of an event and additional event properties. The event core is extended by information about the organism that is acting during the event, one or more instruments used during the event, one or more sensors used during the event, extended measurements or facts linked to the event (deployment), and the data records collected during the event.

Basis for this work is provided by [A standardisation framework for bio-logging data](https://github.com/ocean-tracking-network/biologging_standardization/tree/master), published Sequeira et al. 2021 A standardisation framework for bio-logging data to advance ecological research and conservation. Methods in Ecology and Evolution 12, 996-1007  [https://doi.org/10.1111/2041-210X.13593]( https://doi.org/10.1111/2041-210X.13593).

Similarities exist between biologging data and camera trap data, see work on developing a data model for camera trap data in progress [here](https://docs.google.com/document/d/1DkrjaAyabHc1zqvcJxivTiHp45jQOmGfE4beAtVsUi8/edit#heading=h.avhlbhurvh3v).

Metadata at dataset level is based on the [GBIF metadata profile](https://ipt.gbif.org/manual/en/ipt/latest/gbif-metadata-profile), based itself primarily on the [Ecological Metadata Language (EML)](https://sbclter.msi.ucsb.edu/external/InformationManagement/EML_211_schema/docs/eml-2.1.1/index.html), and the [DataCite Metadata Schema](https://schema.datacite.org/meta/kernel-4.4/).


## 
### Repository

* this repo is now linked to our Slack channel

### License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0)
