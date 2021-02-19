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

## Publisher

A publisher can be any organisation, project or individual requesting a publisher to CyCAT.

| Field name        |  Description           | Required  |
| ------------- |:---------------------------| ---------:|
| `name` | Name of the publisher (full name)| :heavy_check_mark: |
| `short-name` | Name of the publisher (short name) | :heavy_check_mark: |
| `description` | Description of the publisher | :heavy_check_mark: |
| `cycat-uuid` | assigned CyCAT UUID | :heavy_check_mark: |
| `link` | Internet link referencing the publisher | :heavy_check_mark: |

Publisher examples: `mitre`, `circl`, `misp`

## Project

A publisher can request one or more project to CyCAT associated to the publisher namespace.

| Field name        |  Description           | Required  |
| ------------- |:---------------------------| ---------:|
| `name` | Name of the project (full name)| :heavy_check_mark: |
| `short-name` | Name of the project (short name) | :heavy_check_mark: |
| `description` | Description of the project | :heavy_check_mark: |
| `cycat-uuid` | assigned CyCAT UUID | :heavy_check_mark: |
| `link` | Internet link referencing the project | :heavy_check_mark: |
| `license` | License(s) of the project in SPX identifier (array) | :heavy_check_mark: |
| `type` | [Taxonomy type](https://github.com/CyCat-project/cycat-taxonomy) of the project from CyCAT taxonomy | :heavy_check_mark: |
| `scope` | [Taxonomy scope](https://github.com/CyCat-project/cycat-taxonomy) of the project from CyCAT taxonomy | :heavy_check_mark: |
