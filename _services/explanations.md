---
title: "Explanations - supporting documentation on the CyCAT format"
date: 2021-02-24T08:18:35+01:00
featured: true
weight: 1
layout: explanations
---

# General concepts

As decscribed on the (concept page)](https://https://cycat.org/concept/), the CyCAT data-set maintains two main object types:

* Publisher information
* Project information

The former, **publisher** objects, describe unique resources detailing the information on individuals and organisations that wish to share project information. The main purpose is not only to associate information, but also to maintain modification and publishing rights of any information associated to the given publisher. **Publisher** objects are referenced via a unique publisher namespace, which gets registered and created CyCAT.org on request from a CyCAT publisher.

The latter, **project** objects, deal with individual references to Cybersecurity resources. Any such resource is therefore inherently tied to a publisher. **Project** namespaces are created by CyCAT **publishers** under their namespace.

By combining the **publisher** and the **project** namespaces along with an individual UUID ((UUID)](https://en.wikipedia.org/wiki/Universally_unique_identifier)), CyCAT generates a machine-parseable tag for each resource which can be used to reference the description of said resource in other projects, documentation, etc.

The resulting format is a tag in the following format:

`publisher-short-name`:`project-short-name`:`UUID`

This format allows for extending existing **projects** with additional resources, whilst maintaining the ownership of any such extensions under the resource **publisher**'s namespace.

Ultimately the main purpose of both objects is to allow for a simple and standardised lookup mechanism for resources on both concepts.

# For users of the CyCAT data-set

What all of this means in practice, is that CyCAT users can search the data-set on two separate layers, on the **project** layer, when seeking information and references about a given concept (such as att\&ck, playbooks, threat actors, sigma rules) and then further refining the searches via **publishers**.

Whichever scope is queried, the resulting return data will contain a set of objects, each with a simple definition of the object containing the url describing the given concept. When searching for a **project**, consider further filtering the results based on the **publisher** scope.


# For producers of CyCAT data

The first step of encoding a resource reference is making sure that you have a **publisher** namespace reserved. For a full explanation of the **publisher** object, see the (concept page)](https://https://cycat.org/concept/).

The authoritive data-point in the **publisher** object is the `short-name`. When selecting a `short-name`, make sure that the name is as uniquely identifiable and tied to your organisation or person as possible.

It may often be the case that you are encoding information on behalf of a different project, organisation or for yourself as an invidual, consider using alternate **publisher** namespaces when this is the case to hav a clear separation between the role you play in the maintenance of the given resource.

Once the desired **publisher** exists in CyCAT, the next step is to create and reserve a namespace for the given **project** under which the resource belongs. A **project** can define a wide range of topics, be it a tool (such as MISP), a library (such as ATT\&CK) or a common concept (such as threat actors).

Consider separating individual topics within a broad library into separate project names, if your library describes tangentally related concepts, keeping a clear separation between them will make it easier to imediately understand the concerns described by a resource.

As an example, the ATT\&CK framework contains information on attacker techniques as well as threat actor information. This could be separated into the following namespaces:

`mitre`:`att\&ck-threat-actor`:`[uuid]`
`mitre`:`att\&ck-tactics-enterprise`:`[uuid]`

As opposed to:

`mitre`:`att\&ck`:`[uuid]`

The former allows a user to immediately identify the topic of the resource.

Once both a **publisher** and a **project** namespace are created, described and linked, individual resources can be associated under the `publisher`:`project` namespace combination. These are identified by a UUID, a unique identifier assigned to each resource. Keep in mind that a large number of libraries already contain UUIDs for individual resources, in which case it is highly recommended to reuse those UUIDs in CyCAT.
