# FornPunkt Open Data

This repository contains the source code for FornPunkt's open data portal as well as its dataset catalog.

FornPunkts data portal is built with [Snowman](https://github.com/glaciers-in-archives/snowman), a static site generator for SPARQL endpoints. The source of the SPARQL endpoint is a Turtle file describing the FornPunkt data catalog and its contents.

## Source data

The data model used by this repository is based on DCAT 3.0 and VoiD, with a small addition of "[Representing Content in RDF 1.0](https://www.w3.org/TR/Content-in-RDF/)" and Schema.org so that all necessary data can be held in RDF.

### Notable vocabularies

 - [Access right (from the Publications Office of the European Union)](http://publications.europa.eu/resource/dataset/access-right)
 - [Creative Commons Licenses](https://creativecommons.org/about/cclicenses/)
 - [IANA Media Types](https://www.iana.org/assignments/media-types/media-types.xhtml)
 - [Schema.org](https://schema.org/) (`https://schema.org/WebAPI` / `https://schema.org/DataDownload`)

## Development

Prerequisites: Git, Snowman, any backend supporting the SPARQL protocol

### Get the code

```
git clone https://github.com/fornpunkt/open-data.git
```

### Index the data

1. Upload/index `static/data.ttl` into your SPARQL backend.
2. Update snowman.yaml to point to your endpoint.

### Building the site

In the root directory of this repository:

```
snowman build && snowman server
```
