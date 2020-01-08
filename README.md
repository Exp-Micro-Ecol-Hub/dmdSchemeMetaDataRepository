# dmdScheme MetaData Repository
Repository for the metadata created by using dmdScheme based metadata schemes.

## **<span style="color:red">This is a draft document and the repository is not yet functional!</span>**

## Repo structure:

- metadata
	- DIRECTORY.yaml
	- SCHEME1NAME_VERSION1
		- metadata_as_xml_1_.xml
		- metadata_as_xml_2_.xml
		- metadata_as_xml_3_.xml
		- ...
	- SCHEME1NAME_VERSION2
		- metadata_as_xml_1_.xml
		- metadata_as_xml_2_.xml
		- metadata_as_xml_3_.xml
		- ...
	- SCHEME2NAME_VERSION
		- metadata_as_xml_1_.xml
		- metadata_as_xml_2_.xml
		- metadata_as_xml_3_.xml
		- ...
	- db.sqlite
		SCHEME1NAME_VERSION1.sqlite
		SCHEME1NAME_VERSION2.sqlite
		SCHEME2NAME_VERSION.sqlite
	- db.sqlite
		SCHEME1NAME_VERSION1.sqlite
		SCHEME1NAME_VERSION2.sqlite
		SCHEME2NAME_VERSION.sqlite

As everything is text, a csv should be sufficient. 
Otherwise, an sqlite would be more robust, but not that suitable for github. For the 
moment, we should leave it as a csv for the moment and master.

### File DIRECTORY.yaml
This is a yaml file, with the following structure:
- top level: `NAME_VERSION` of the scheme
	- `name`: Name of the scheme
  	- `version`: Version of the scheme
  	- `creator`: creator of the scheme
  	- `info`: Info to the metadata

## Upload of new metadata

The upload is not automated yet. A possibility would be to have an R package which is 
- cloning the repo
- adding the metadata to the directory
- adding the metadata to the db.*
- add the relevant info tho the DIRECTORY.yaml file
- commits the changes
- pushes the changes to github


