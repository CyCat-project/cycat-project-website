---
title: 'FAQ'
date: 2020-01-29T17:01:34+07:00
layout: page
bodyClass: page-about
---
## Table of Contents

* [Initiative\-Related Questions](#initiative-related-questions)
  * [Reinventing The Wheel](#reinventing-the-wheel)
  * [Nature Of The Initiative](#nature-of-the-initiative)
  * [CyCAT Team](#cycat-team)
  * [Community Behind CyCAT](#community-behind-cycat)
* [Service\-Related Questions](#service-related-questions)
  * [Curation And Validation \- I](#curation-and-validation---i)
  * [Curation And Validation \- II](#curation-and-validation---ii)
  * [API Functionality Backed By a Website](#api-functionality-backed-by-a-website)
  * [Data Normalisation](#data-normalisation)
  * [Rule Resilience Against Small Attack Variations](#rule-resilience-against-small-attack-variations)
  * [Onboarding Existing Cybersecurity Repositories](#onboarding-existing-cybersecurity-repositories)
  * [Links Between Existing Cybersecurity Repositories And CyCAT](#links-between-existing-cybersecurity-repositories-and-cycat)
  * [Tool Versions And Identifiers](#tool-versions-and-identifiers)
  * [Identifiers For Techniques vs\. Tools](#identifiers-for-techniques-vs-tools)
  * [ATT&amp;CK Mapping In CyCAT](#attck-mapping-in-cycat)
  * [API Output](#api-output)
  * [OData Support](#odata-support)
  * [Identifier Deprecation And Linking](#identifier-deprecation-and-linking)
  * [Threat Actor Identifiers](#threat-actor-identifiers)
  * [Governance And Namespaces](#governance-and-namespaces)
* [Taxonomy\-Related Questions](#taxonomy-related-questions)
  * [Splitting Respond](#splitting-respond)
  * [Relationships Between Catalogue Entries \- I](#relationships-between-catalogue-entries---i)
  * [Relationships Between Catalogue Entries \- II](#relationships-between-catalogue-entries---ii)
  * [Tool Capability Specification](#tool-capability-specification)
  * [Rule Capability Specification](#rule-capability-specification)
  * [Item Versioning](#item-versioning)
  * [Datasets And Their Verification](#datasets-and-their-verification)
  * [Data Model](#data-model)
  * [Taking Into Account Friendly (e\.g\. Red Team) Testing](#taking-into-account-friendly-eg-red-team-testing)

## Initiative-Related Questions

### Reinventing The Wheel

_Do you compete with project X?_

No, we do not compete with any project. Our goal is to reference the various projects in the cybersecurity field. The goal is to provide more synergies and visibility among the different projects.
The aim is not to replace any existing initiative in cybersecurity but to link and offer better visibility to all project owners and user communities.

### Nature Of The Initiative

_Is CyCAT.org a for-profit initiative?_

No. CyCAT.org is a non-profit initiative ran by a [team of motivated people](/team) to catalogue and crosslink cybersecurity resources. All our content, tools and dataset are or will be released under an open source license or even put in the public domain.

### CyCAT Team

_Who is behind CyCAT.org?_

We are experienced, community-oriented cybersecurity professionals who have at heart to help our fellow defenders keep threats at bay while making their life simpler. [Meet the team!](/team/)

### Community Behind CyCAT

_Who is helping CyCAT.org?_

CyCAT is a collaborative effort and we would like to [thank the people who helped us](/acknowledgment/).

## Service-Related Questions

### Curation And Validation - I

_While I really appreciate the initiative, curation might become a hefty task as the initiative takes off and the number of submissions for entries into CyCAT grows. Apart from the quality of the content, the correct mappings, etc. need to be validated.
I can imagine there will be a moderation team that can take care of this. The most important part will be the community that will take an active role in keeping the flow of new and updated projects coming in._

Indeed, you point to an important element for CyCAT’s success. It is already covered in the [white paper](https://cycat.org/services/whitepaper/):

> Essential features such as version control, crowd sourced vetting and quality control as well as deprecation will be integrated from the outset.

### Curation And Validation - II

_I don't see the number of entries (detections, playbooks, ...) as a problem anymore. However, many open source detections in projects such as SIGMA are not working because of the lack of proper testing and community support. This isn’t the fault of the maintainers of these projects. The IT security community loves to use open source projects but their willingness to contribute back is very limited. We need to find a way to keep the IT security community more engaged in these kinds of initiatives. Otherwise, this will also be a problem for you, e.g. when users use CyCAT to query for detections and these detections aren’t working. This could drive them away from using and contributing to CyCAT._

Indeed, you point to an important element for CyCAT’s success. It is already covered in the [white paper](https://cycat.org/services/whitepaper/):

> Essential features such as version control, crowd sourced vetting and quality control as well as deprecation will be integrated from the outset.

### API Functionality Backed By a Website

_While making the different CyCAT entries searchable over an API is definitely a big improvement, it is very important to also have a website which leverages the API._

We do agree and this is our intention: provide an API, backed by a publicly accessible website.

### Data Normalisation

_Data normalisation is still an unsolved issue and it will be a significant problem for initiatives like yours. When every detection rule project uses their own data normalisation, the result of your API for detection rules can be very hard to understand because users would need to understand, beside the different query languages, the different field extractions and mappings used by the different detection rule projects._

We fully agree with your statement. However, CyCAT, as a ‘meta’ catalogue, will not tackle this aspect. If we take a library analogy, CyCAT will point you to the book, giving some meta-information about it but not its content. So if you make an API call to CyCAT for detection rules, it will tell you what detection rules are available, where, and for what purpose (and in a future version indicate in which coherent ‘packages’ they are included), but not their content nor how you should parse them.

### Rule Resilience Against Small Attack Variations

_Aside from quality, another issue is the resilience of detection rules. Quality makes sure the detection rule works for a specific TTP and the IT security community’s feedback and contributions help to reduce the number of false positives. The next step is to make the rules resilient against small variations of the same attack._

Through an enhanced taxonomy or the right data modelling, CyCAT users would be able to identify the relevance of a rule in broad terms (e.g. `stable`/`experimental`, `full`/`partial` coverage). But for a future iteration, we would need to reflect with the community on how to embed a bit more granularity into CyCAT to allow resource owners to indicate what attack variations a rule would cover.

### Onboarding Existing Cybersecurity Repositories

_Do you have a process to rapidly onboard existing repositories, e.g. SIGMA, ThreatHunterPlaybook or CAR? Will you do that or would it be the responsibility of the resource owners?_

The alpha version of CyCAT, which we intend to release on 1 June 2021, during the EU ATT&CK Community workshop, will contain a number of existing repositories, to demonstrate the value of our proposition and identify potential issues that need to be addressed in future CyCAT iterations. Owners of repositories which we wouldn’t be able to integrate in the alpha version will be invited to reserve a namespace in the catalogue to integrate their resources.

### Links Between Existing Cybersecurity Repositories And CyCAT

_Should resource owners consider contributing by linking their repositories to CyCAT?_

Repository owners should consider linking their resources to CyCAT, by reserving a namespace and providing some metadata and descriptions. Work is undergoing to specify mandatory vs. optional information owners should integrate in CyCAT, depending on the various taxonomy scopes. **If you have any suggestion as to what information you’d like to see for CyCAT entries, please let us know**.

### Tool Versions And Identifiers

_You mention tools. Would Mimikatz get an identifier?  Is it expected that Mimikatz would use the same one for its entire lifetime? Should different platforms of the same tool get a different identifier? How CyCAT would manage situations where a researcher requests an identifier on a project’s behalf, but then the owner requests one themselves?  If tools get identifiers, what about products? Would there be any overlap with any existing software inventory scheme used by CERTs or other organisations._

That’s an excellent question that needs careful consideration as it may have profound impacts on the usability of CyCAT for both resource owners and users. We can imagine that, for a tool such as Mimikatz, the author would apply for a ‘Mimikatz’ namespace, in which they integrate identifiers corresponding to specific versions, augmented by an indication of their status (`stable`/`experimental`) and the platforms they run on.

Ideally, only resource owners should be able to apply for a namespace and programmatically and inexpensively generate UUIDs, instead of researchers or users. This will also need careful thought to avoid catalogue pollution/poisoning.

### Identifiers For Techniques vs. Tools

_Will identifiers be assigned for both techniques (e.g. password spraying) and tools embodying them?_

_Is there a namespace for these to exist in?  i.e. identifier `1234` for `tools/passwordspray/Office365/foobar` v. `vulns/heartbleed/poc-python`.  If not, I wonder how duplication/overlap checking will be handled when there are 1.000 or 10.000 identifiers._

A taxonomy (e.g. ATT&CK) will have its own namespace. Within that namespace, techniques will have their own identifiers. Tools will also have their own UUIDs and in a future iteration of CyCAT, links will be made between the two so users will be able to select all tools that support a certain technique. Users will also be able to obtain coherent ‘packages’ covering the techniques they are interested in and the related tools and to which areas or scopes they apply.

As for namespaces, they would correspond to organisations / resource owners behind the various entries in CyCAT. This way, we would ensure that a certain tool, technique, vulnerability, etc. isn’t duplicated.

### ATT&CK Mapping In CyCAT

_Should there be a 1-1 mapping of CyCAT identifier for every MITRE technique? Would subtechniques get their own CyCAT identifier?_

ATT&CK will have its own namespace. And every entry in ATT&CK should have its existing UUID transposed to CyCAT as a UUID within the ATT&CK namespace.

### API Output

_I assume the API will return metadata about CyCAT entries? Like the timestamp of creation and descriptive text in whatever language translations exist for it? Every identifier should have a version field. When you request the metadata about an identifier, it should return the version so you can extend it going forward._

The API will indeed return metadata about the queried identifier such as the ones you mention. However, CyCAT will not handle version control for the resource owners. Instead, it would provide some broad elements (`stable`, `latest`, `experimental`, `deprecated`…).

### OData Support

_I assume the API will support OData syntax (this allows filters, operators like TOP N etc.)?_

Filtering and additional functionality will be integrated in the API and OData seems like a good, industry-standard solution to do so.

### Identifier Deprecation And Linking

_I think you will need some concept of a forward link in these identifiers when the community or CyCAT realises they want to deprecate an older identifier in favour of a newer one, to facilitate consolidation for example, while not breaking documentation or products that use this._

Identifiers will indeed carry some sort of characterisation, including their status (e.g. `in-use`, `deprecated`). This will impact how the relationships they have with other identifiers within the catalogue and the packages in which they are included.

### Threat Actor Identifiers

_I can imagine someone trying to get a CyCAT identifier for threat actors.  Would APT28 get a different one than STRONTIUM and yet another one for FANCY BEAR? This wades into the attribution space which, as you know, is subject to highly divergent opinions at times._

We are not currently considering integrating a ‘threat actor’ type in the taxonomy. However, owners of resources which have a CTI aspect (e.g. a tool used by a certain threat actor) could specify optional metadata to provide more information to those querying CyCAT.

### Governance And Namespaces

_How and who decides to hand out identifiers? Can organisations request a set of identifiers up front? I can imagine large organisations wanting to consolidate how they create/assign these for their products rather than have individuals reach out to you for every specific product they want to add to the catalogue._

CyCAT will allow resource owners, either as organisations or individuals, to apply for namespaces for their resources. Once they obtain namespaces, they will be able to freely generate identifiers within these namespaces for their resources.

## Taxonomy-Related Questions

### Splitting Respond

_The `respond` scope in the taxonomy is quite wide. Why don’t you split it into `contain` and `eradicate`, that might include other defined scopes, such as `investigate`, `recover`, `identify` or even `detect`, depending on the point of view, a context or a specific use case?_

While we tried to adhere to the [NIST CSF](https://www.nist.gov/cyberframework), your question highlighted the fact that CyCAT’s taxonomy doesn’t limit itself to the 5 functions of the framework. It includes, for example, an `investigate` scope that doesn’t exist in the NIST CSF, not to mention `exploit`, `train` or `test`. We will thus closely look at adding scopes, when relevant, corresponding to specific categories and subcategories, instead of sticking to higher-level functions only. e.g. for `respond` we could have `respond-analysis` or `respond-mitigations`.

As for the `identify` scope in the taxonomy, it corresponds to the corresponding _Identify_ function in the NIST CSF and not to the identification of a piece of evidence in the _Respond_ function, which is which is covered by _RS.AN (Analysis)_.

### Relationships Between Catalogue Entries - I

_To make CyCAT a success, one important element is relationships between entries, on an object level, but also between objects and object types. More concretely, a possibility to specify a relationship such as "rule A is of type Sigma rule" and another relation that specifies "Tool X converts Sigma rules into queries" or ‘Rule B -> Yara Rule -> Tool B scans for Yara matches in the file system/memory’ would be essential._

As mentioned in the [CyCAT white paper](https://cycat.org/services/whitepaper/):

> Finally, the system will, in a future iteration, facilitate interlinking resources that could be used in conjunction for an improved capability in coherent “packages”. Such “packages’’ could then be deployed by less mature entities as plug-and-play solutions to save time and defend themselves properly, while avoiding the pitfalls resolved by early adopters or more mature organisations.

So while the alpha version, which we intend to launch at the next EU ATT&CK Community workshop, on 1 June 2021, will not support resource interlinking, we do intend to include such an important feature in a future iteration.

### Relationships Between Catalogue Entries - II

_The different taxonomy types (detections, playbooks, ...) need to work together in order to be useful for CyCAT users. The detections need to fit to the data normalisations and the output needs to fit to the playbook. However, there is no established standard in data normalisation which would be your interface between log data and detection. Additionally, there is no standard between output of a detection and input into a playbook. If we don't solve these problems, the usability of projects like CyCAT will remain limited._

As mentioned in the [CyCAT white paper](https://cycat.org/services/whitepaper/):

> Finally, the system will, in a future iteration, facilitate interlinking resources that could be used in conjunction for an improved capability in coherent “packages”. Such “packages’’ could then be deployed by less mature entities as plug-and-play solutions to save time and defend themselves properly, while avoiding the pitfalls resolved by early adopters or more mature organisations.

So while the alpha version, which we intend to launch at the next EU ATT&CK Community workshop, on 1 June 2021, will not support resource interlinking, we do intend to include such an important feature in a future iteration.

Regarding data normalisation, and beside the [answer below](#data-normalisation), we will definitely need to standardise the way we conceive the aforementioned packages, but not necessarily their content, such as the rules they would contain. A package might include various rules, in various formats, with tools, some of which might work with a subset but not all of these rules.

Our aim is to use CyCAT as a vehicle to make concrete steps to ‘weed the jungle’ and favour normalisation and standardisation.

### Tool Capability Specification

_There is a need to specify the capabilities of tools. Does a Yara scanner scan only files? Or also memory? How is the maturity level of the functionality? To support this, the taxonomy needs to be extended. e.g. a tool entry in CyCAT should contain information such as `capability:file-scan=stable, capability:memory-scan=experimental`._

_This should be kept optional, to make contributions to CyCAT easy, but it would be a great resource to pick the best tool for a specific use case. This could be accomplished with additional taxonomies which could be used to tag CyCAT items._

This is a great suggestion. We need to think carefully as to how to take it into account in the taxonomy, in a simple, elegant way. Specifying a taxonomy’s type capability, be it a tool, a rule (`endpoint-detection only`, `network-detection only`) or a mitigation (`full`, `partial`) will indeed help the community pick the best entry for the task at hand or know its limitations if any.

### Rule Capability Specification

_There is a need to specify capabilities of detections. What purpose is a rule for? Do I want an alert that rings me out of the bed on Saturday night? Is this something that can wait until Monday morning? Is the intention of the rule to generate leads in threat hunting projects? Or is this just an event we want to see in a malware analysis sandbox run like the creation of a mutex?_

There is an ongoing reflection on adding a purpose tag to SIGMA to indicate the intent behind the rules, because it turns out that the classical info-to-critical levels are not sufficient to express this aspect. It would also make sense to reuse MISP taxonomies or parts of it like `false-positive:risk` in CyCAT. The [SIGMA rules specification](https://github.com/Neo23x0/sigma/wiki/Specification#rule-identification) could also be an inspiration for this purpose.

Your point is valid but we believe that rule capability specifications, other than a few basic ones such as `stable` vs. `experimental` or `endpoint` vs. `network` and a few others covered by the [SIGMA rules specification](https://github.com/Neo23x0/sigma/wiki/Specification#rule-identification) shouldn’t go into CyCAT.

Any additional information should be specified by the rule authors, in their respective rule descriptions or taxonomies. CyCAT could, in a future iteration, display this additional information if the author makes it available over an API for example. But this has to be carefully designed and reflected upon to avoid any scalability issues down the road.

Please note that, as mentioned in the [white paper](https://cycat.org/services/whitepaper/), we envisage to address this in another way, by using coherent ‘packages’ that would interlink several resources with similar or complementary capabilities.

### Item Versioning

_There should also be a clear specification how a version of an item is referenced in CyCAT. Creating a new identifier for every minor change causes a lot of items which could render such a catalogue useless. Accepting bigger changes without a new identifier makes identification imprecise. Adding a versioning attribute adds complexity. In the [specification for SIGMA](https://github.com/Neo23x0/sigma/wiki/Specification#rule-identification), a middle ground was chosen, relying on implicit Git versioning. Will CyCAT be also backed by a Version Control System?_

CyCAT will not cover version control for the entries it will include (the version control mentioned in the white paper applies to CyCAT itself). This is up to the various resource owners to implement. If you are looking for a tool for example, CyCAT will provide general meta-information (we are currently working on what minimal description must be provided by the resource owners) and point you to the location where you can find it, indicating some broad information (`stable`, `latest`, `experimental`, `deprecated`...) if applicable.

### Datasets And Their Verification

_CyCAT should incorporate datasets that could be used to verify (i.e. test) CyCAT entries.We could thus link a detection rule to a sample or a log file in a dataset for verification purposes._

That’s a very good suggestion and we have accepted a pull request that covers this aspect.

### Data Model

_The taxonomy should be extended or replaced by a data model which supports more expressiveness. Something like MISP objects could be appropriate._

This is a very good suggestion and we will need to reflect on how we could conceive a powerful, yet simple data model to support such expressiveness. This will probably not be offered in the alpha version, which we intend to release in June 2021 but could be integrated in a follow-up iteration.

### Taking Into Account Friendly (e.g. Red Team) Testing

_You may want to integrate Red Team tests in the taxonomy. This would capture atomic Red Team and CALDERA tests._

This is a good idea and it has been taken into account in the taxonomy by adding a `test` scope and a `dataset` type.
