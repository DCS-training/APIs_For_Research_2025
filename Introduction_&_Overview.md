# Introduction & Overview

## Table of Contents

- [What is an API?](#what-is-an-api)
- [Web APIs & Software libraries](##web_apis_&_software_library_apis)
- [API types](##api_types)
- [REST APIs](#rest-apis)
- [Example APIs](####-example-apis)
- [Documentation](#-documentation)
- [File Formats](#-file-formats)
- [Use cases for Research](#-use-cases-for-research)
- [Further resources](#-resources)

# APIs for Research

Application programming interface (API)s are communication tools between software platforms, that allow different programs to interoperate with each other.
In digital humanities research, they are regularly used for accessing and retrieving data from digital collections with open access (archives, libraries, museums) and linking these entities to ongoing research. 

APIs have many use cases outside of this for relevant parties like developers, institutions wishing to create and share resources and so forth, we will mention these but not delve into them. The focus of the workshop is applied uses of APIs for researchers and practical guidance for interacting with existing APIs and collecting data. 

# What is an API?

An API is essentially a set of rules and endpoints that let software retrieve or interact with data from a remote system without needing to scrape websites or manually download files. The URLs we examine are an important feature in using APIs when accessing web APIs specifically.

Each endpoint typically corresponds to a certain type of resource or function (e.g.
an endpoint for “objects” might return a list of objects in a collection). The server responds with a representation of the data, usually in a structured format like JSON (JavaScript Object Notation), which is a lightweight text format for data exchange.

## Web APIs & Software Library APIs

APIs can be sorted into two categories: Web based, and software library based.

### API types
> A non-exhaustive list 
GraphQL: Client-defined queries for precise data retrieval.
SPARQL: Query language for RDF and semantic web data.
REST: Web service style using HTTP methods for resource access
...........

#### Example APIs
1. Europeana: Online portal to Europe’s cultural heritage collections.
2. Open Library: Open, editable catalog of books from around the world.
3. ORCID: Persistent researcher ID system for scholarly identity.
4. Crossref: Organisation providing DOIs and metadata for scholarly works.
5. Smithsonian: U.S. group of museums and research centers with vast collections.
6. Victoria & Albert Museum: UK museum focused on art, design, and decorative arts.
7. The British Library: National library of the UK with extensive global collections.


### Other useful things to know
- IIIF: A standardised framework for delivering high-quality images and metadata, allowing museums, libraries, and archives to share, compare, and display digital images using common APIs

### REST APIs
REST (Representational State Transfer) is a popular architectural style for web services. A REST API is an interface that uses standard HTTP protocols (the same that power the web) to allow clients to retrieve or manipulate data. In practice, this means the API exposes one or more endpoints – specific URLs that represent data resources – and clients make HTTP requests (like GET or POST requests) to those endpoints.

### Status codes
Can spell trouble or success. Status codes when working with HTTPS based API requests let you know what the status of a given request is. Here are some examples:

- 200 - OKAY
- 404 - Not found
- 403 - Forbidden

Status codes are explained further in Documentation (See below), and are useful to quote for crowdsourced troubleshooting.

# Documentation
The user manual for an Application Programming Interface. They provide clear, structured instructions that explain how to use an API. It typically includes:
What the API does;
Available endpoints or functions;
Required inputs (parameters);
What the outputs look like;
Examples of requests and responses

In practice:
- Specific coding packages for R and Python that are built for accessing APIs have their own documentation that is required reading
E.g. tubeR - an R package for accessing the Youtube Data API; python-youtube - a Python Package for the same.


# File formats 

## JSON JavaScript Object Notation, XML Extensible Markup Language and RDF
J-SON are a common file format for configuration, APIs, and data exchange

```json
{
  "name": "Alice",
  "age": 25,
  "languages": ["English", "Spanish"]
}
```


XML is a text based file format 
A text-based format for storing and transporting structured data using custom tags. It’s both human-readable and machine-readable, and is commonly used in web services, configuration files, and data exchange.
```xml
<?xml version="1.0" encoding="UTF-8"?>
<Person>
    <Name>Alice</Name>
    <Age>25</Age>
    <Languages>
        <Language>English</Language>
        <Language>Spanish</Language>
    </Languages>
</Person>
```


RDF (Resource Description Framework) File Format

RDF is a standard model for representing structured information about resources on the web. It expresses data as triples: subject – predicate – object, which makes it easy to link and integrate data across different sources
It is ideal for describing relationships between resources, e.g., authors, books, and institutions
For example: 

```turtle
@prefix ex: <http://example.org/> .

ex:Alice ex:hasAge 25 .
ex:Alice ex:speaksLanguage ex:English .
ex:Alice ex:speaksLanguage ex:Spanish .
```


# Use cases for Research

Public APIs are the most ideal and those issued by established institutions, public and private have formed incredible resources for researchers.

- (GLAM) - there has been a steady rise in digitisation in the public sector and many organisations - national and regional - offer APIs and open digital resources.
- The NHS - The NHS offers multiple different APIs for aggregated healthcare data 
- Government portals - UK regional and national governments offer API data on different socio-economic, climatic and other data through different organisations. 

In addition - private enterprise use APIs and many social media companies offer these to researchers. Many require a research application and are costed in some cases:
- Google
- META
- X
- TikTok

# Other use cases

Other than generating data, developers  are interested in the integration of multiple APIs to create dynamic environments pulling in data from various sources, adding new features, extrapolating on existing frameworks and general flexibility that APIs offer them.

For example Tools like Dimensions automatically pull a researcher’s publications and citations linked to their ORCID ID.
Google Arts & Culture uses Smithsonian data to showcase artworks, artifacts, and images in digital exhibits.


# Limitations & considerations

Rate limits - The amount of individual calls a program can make to an API. Researchers are often given a quota (e.g. 200 calls every minute) that limits access.
- Note in our workbook we will encounter some of these limits (ie.e the Met museum recommends no more than 80 requests per second)


Running locally versus on cloud based platforms
Locally: Convenient for development and testing; may face network or resource limitations if running on a lite-machine e.g. a notebook

Cloud: Scales better for large datasets and multiple users; may incur costs or require specific permissions. Many Cloud platforms are free or low cost

# Resources
API Documentation

GraphQL Docs
 – Official guide to GraphQL queries.
 - [GraphQL](https://graphql.org/learn)

SPARQL Tutorial
 – Learn querying RDF datasets.
 - [SPARQL](https://www.w3.org/TR/rdf-sparql-query/)

REST Guide
 – Principles and best practices for REST APIs.
 - [REST](https://restfulapi.net)

Digital Libraries & Collections

Europeana Collections
 – Europe’s cultural heritage portal.
 - [Europeana Collections:](https://www.europeana.eu/en)

Open Library
 – Free, editable catalog of books.
 - [Open Library](https://openlibrary.org)

Smithsonian Open Access
 – Access images & metadata from Smithsonian museums.
 - [Smithsonian Open Access](https://www.si.edu/openaccess)

V&A Museum API
 – V&A museum collection data.
 - [V&A Museum API:](https://developers.vam.ac.uk/)

British Library Digital Collections
 – Digitized books, manuscripts, and images.
 - [British Library Digital Collections:](https://bl.iro.bl.uk/collections/64e3804a-788a-4c4b-962c-ae180d955455?locale=en)

## Research Tools

ORCID
 – Persistent researcher identifiers.
 - [ORCID](https://orcid.org/)

CrossRef
 – Metadata and DOI registry for scholarly works.
 - [CrossRef](https://www.crossref.org/)

Standards & Frameworks

IIIF
 – Standardized APIs for high-quality images.
 - [IIIF](https://iiif.io/)

JSON Guide
 – Overview of JSON structure and usage.
 - [JSON](https://www.json.org/json-en.html)

XML Guide
 – Reference for Extensible Markup Language.
 - [XML:](https://www.w3.org/XML/)

## Developer Tools

Postman
 – API testing and development tool.
 - [Postman](https://www.postman.com/)

Swagger/OpenAPI
 – Tools for designing and documenting APIs
 - [Swagger / OpenAPI](https://swagger.io/)









