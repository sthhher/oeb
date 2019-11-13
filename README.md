# OEB

My project is to make a json schema to validate the tools of the openebench website.

This json schema validator we want to linked to two ontologies because we have that validation in mongo with collections and we have one more general.

Also, to do it more general, we want a PURL, a permanentID in the repository w3id.org.

## OEB-ontologies
We want to do the validation that do mongo with collections with two ontologies. One about formats (FASTA, JSON, TAR,...) linked to ontology EDAM, and other ontology with datasets importing the other ontology and linked to that. 

### oebDataFormats ontology
Based on [EDAM](http://edamontology.org/EDAM.owl), **oebDataFormats** imports it with some extra data formats (classes) and properties

- New classes: TAR, Log, ERR
- New properties: file_extension

### OEBdatasets ontology
Describes the different types of datasets involved in OpenEBench platform. **OEBdatasets** imports oebDataFormats' ontology to better define dataset's files adding 'file_type' properties.


## OpEB-VRE-schemas

### json_schema_mongodb.json
A json schema for validate in mongodb. 

### tool_schema_internal_MuG.json
A json schema for MuG.

### tool_schema_internal_OEB.json
A json schema for OEB. Is to validate all the data the developer introduce. Also we have a mongo collection with extensions of file_type and what datasets accept. For example: dataset aggregation oly accept file_type JSON and TAR and JSON has extension of "json" and TAR extension of "tar".

### json_schema_FAIRfication_OEB.json
A json schema to validate with  fairtracks validator (https://github.com/fairtracks/fairtracks_validator).


## w3id-PermanentID
The way about how we have done the document .htaccess to get a permanentID, PURL.

### oebDataFormats
The PURL of oebDataFormats. We linked a permament ID with the raw of oebDataFormats ontology on inab. (https://raw.githubusercontent.com/inab/OEB-ontologies/master/dataFormats.owl)

### oebDatasets
The PURL of oebDatasets. We linked a permament ID with the raw of oebDatasets ontology on inab. (https://raw.githubusercontent.com/inab/OEB-ontologies/master/oebDatasets.owl)
