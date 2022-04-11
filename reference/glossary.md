# Glossary

## Data Coordinator

The Data Coordinator acts as a liaison between internal Information Technology staff, organizational programs and leadership, and portal managers.

They are best positioned to convey to the appropriate parties any specific needs of the open data portal and program. They are trusted partners in open data within their organization.

## Data Custodian

The Data Custodian is the person most knowledgeable about how the data is stored and protected and have technical knowledge on how to query and extract data.

They advise and help with data access and navigate technical options for automation.

## Data Steward

The Data Steward is the person most knowledgeable about the data including the sources, collection methods, and limitations.

They prepare data for publishing on the portal and work with Data Custodians for any system access needs and work with the Data Coordinator for publishing approval.

## Dataset

Within data.ca.gov, a dataset (or data set) is a collection of data and resources. [See definition of resources](glossary.md#resources).

## Extract, Load, Transform (ELT)

ELT is the process of extracting data from one or multiple sources and loading it into a data warehouse. Instead of transforming the data before it is written, ELT takes advantage of the system where the data is to be stored to perform the data transformation. This is another approach to automating data updates to the open data portal. In this case the final transformed dataset in the warehouse is synced to the open data portal.

ELT is an alternative to the [ETL process defined below](glossary.md#extract-transform-load-etl).

Read [this article for more information on the differences between ELT and ETL](https://blog.panoply.io/etl-vs-elt-the-difference-is-in-the-how).

## Extract, Transform, Load (ETL)

ETL is a type of data integration that consists of three steps (extract, transform, load) used to blend data from multiple sources. During this process, data is taken (extracted) from a source, converted (transformed) into a format that can be analyzed, and stored (loaded) into a data warehouse or other system. This is one common approach to automating data updates to the open data portal.

ETL is an alternative to the [ELT process defined above](glossary.md#extract-load-transform-elt).

Read [this article for more information on the differences between ELT and ETL](https://blog.panoply.io/etl-vs-elt-the-difference-is-in-the-how).

## Flat file

A flat file is an informal term for a single table of data from which all word processing or other structure characters or markup have been removed. A flat file stores data in plain text format. Because of their simple structure, flat files can only be read, stored and sent. Comma-separated-values (CSV) files are one of the most common types of flat files. They are text files where the fields are separated by commas and each row is a new line.

## Harvesting

Harvesting is a process where the data portal automatically imports (“harvests”) datasets from multiple CKAN websites and other non-CKAN sources into a single CKAN website. This automated process is what enables the statewide portal to contain data from other agency and department portals.

To harvest a source catalog, there must be a public interface to a data file that represents the catalog in a [DCAT-US compliant format](https://resources.data.gov/resources/dcat-us/).

The harvests are set up and monitored by system administrators of the portals. It is not something a publisher needs to worry about when publishing.

## Machine Readable

Information or data that is in a format that can be easily processed by a computer without human intervention. To be machine readable, data must be structured in an organized way. [CSV](https://data.ca.gov/open-data-glossary#csv), [JSON](https://data.ca.gov/open-data-glossary#json), and [XML](https://data.ca.gov/open-data-glossary#XML) among others, are formats that contain structured data that a computer can automatically read and process.

## Personal Health Information (PHI)

Personal health information, also referred to as protected health information, is any information about health status, provision of health care, insurance information and other data that a healthcare professional collects to identify an individual and determine appropriate care.\
\
Under the [Health Insurance Portability and Accountability Act](https://www.cdc.gov/phlp/publications/topic/hipaa.html#:\~:text=The%20Health%20Insurance%20Portability%20and,the%20patient's%20consent%20or%20knowledge.) (HIPAA), data is considered PHI if it includes one or more of the [18 identifiers listed here](https://www.hipaajournal.com/what-is-considered-protected-health-information-under-hipaa/). If these identifiers are removed, the information is considered de-identified protected health information, which is not subject to the restrictions of the [HIPAA Privacy Rule](https://www.hhs.gov/hipaa/for-professionals/privacy/index.html#:\~:text=The%20HIPAA%20Privacy%20Rule%20establishes,certain%20health%20care%20transactions%20electronically.).

## Personally Identifiable Information (PII)

Personally identifiable information is any data that can be used to identify a specific individual. Examples include a full name with Social Security number, mailing or email address, or phone number.

## Resources

Within data.ca.gov, resources are the actual files, APIs or links that are being shared through the portal. Resource types include csv, html, xls, json, xlsx, doc, docx, rdf, txt, jpg, png, gif, tiff, pdf, odf, ods, odt, tsv, geojson and xml files. If the resource is an API, it can be used as a live source of information for building a site or application.
