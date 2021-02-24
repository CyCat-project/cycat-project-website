---
title: "CyCAT - Core Concept"
date: 2021-02-19T01:33:46+10:00
featured: true
weight: 1
layout: service
---

# Concept of CyCAT url

A CyCAT url is composed of a publisher short name, a project short name and the associated UUID of the specific item. An item can be any part of the collection produced
by this publisher under a specific project. The CyCAT url is composed of two namespaces separated by colon and a final UUID appended after a colon. The CyCAT url is in UTF-8 format.

`publisher-short-name`:`project-short-name`:`UUID`

## What is an UUID?

A [universally unique identifier (UUID)](https://en.wikipedia.org/wiki/Universally_unique_identifier) is a 128-bit number used to identify information in computer systems also known as GUID.
CyCAT uses such UUID to reference items produced in a collection. CyCAT, by default, will use any existing UUID already assigned by the publisher. If not present or there is no item present,
a fixed value is then calculated from the UUID namespace of CyCAT combined with `publisher-short-name:project-short-name`.

## Publisher namespace

A publisher can be any organisation, project or individual requesting a publisher to CyCAT.

| Field name        |  Description           | Required  |
| ------------- |:---------------------------| ---------:|
| `name` | Name of the publisher (full name)| :heavy_check_mark: |
| `short-name` | Name of the publisher (short name) | :heavy_check_mark: |
| `description` | Description of the publisher | :heavy_check_mark: |
| `cycat-oid` | assigned CyCAT OID | :heavy_check_mark: |
| `link` | Internet link referencing the publisher | :heavy_check_mark: |
| `timestamp` | Last update of the publisher record (unix timestamp) | :heavy_check_mark: |
| `maintainer` | owner, external, cycat | - |

Publisher examples: `mitre`, `circl`, `misp`

## Project namespace

A publisher can request one or more project to CyCAT associated to the publisher namespace.

| Field name        |  Description           | Required  |
| ------------- |:---------------------------| ---------:|
| `name` | Name of the project (full name)| :heavy_check_mark: |
| `short-name` | Name of the project (short name) | :heavy_check_mark: |
| `description` | Description of the project | :heavy_check_mark: |
| `cycat-oid` | assigned CyCAT OID | :heavy_check_mark: |
| `link` | Internet link referencing the project | :heavy_check_mark: |
| `license` | License(s) of the project in SPX identifier (array) | :heavy_check_mark: |
| `type` | [Taxonomy type](https://github.com/CyCat-project/cycat-taxonomy) of the project from CyCAT taxonomy | :heavy_check_mark: |
| `scope` | [Taxonomy scope](https://github.com/CyCat-project/cycat-taxonomy) of the project from CyCAT taxonomy | :heavy_check_mark: |
| `timestamp` | Last update of the project record  (unix timestamp)| :heavy_check_mark: |
| `maintainer` | owner, external, cycat | - |

## URL example

## How to generate a CyCAT url for non-registered url or missing item in a collection

CyCAT has a fixed UUID namespace `690b3b43-d689-481c-aa61-5351963a36f2`.

```shell
% uuidgen --sha1 -n "690b3b43-d689-481c-aa61-5351963a36f2" -N "samratashok:nishang:"
2605ff5e-342c-5326-8744-96a34b7e581e
```
