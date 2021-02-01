---
title: "Whitepaper - CyCAT.org - The Universal Cybersecurity Resource Catalogue"
date: 2021-01-29T12:33:46+10:00
featured: true
weight: 1
layout: service
---

# Problem definition

Our society is more and more dependent on information systems and the disruption by cyberattacks is an ever-increasing risk. As adversaries are becoming more astute and organised, defenders are also doing so. In the past few years, several initiatives have sprung up while numerous tools, products, frameworks and methodologies have been released to prevent, detect and respond to a large variety of threats. MITRE ATT&CK®, NIST’s Cybersecurity Framework, YARA, SIGMA, JUPYTER or even Markdown are but a few that have been taken up by the community as efficient ways to document insights and make them actionable.

In addition, companies, security researchers and other parties are constantly contributing new software, refining and improving existing code, producing detection rules and mitigating controls in various shapes and formats, and not always properly advertised nor documented. Moreover, many of these are being developed with little consideration for or lack of knowledge of similar, prior art. As a result the wealth of available resources and insights remains untapped while effort duplication and functionality overlap can sometimes lead to inefficiencies and end user puzzlement.

We believe that this is mainly due to three, intertwined factors:

- The staggering number of initiatives, tools, detection rules produced in a decentralised manner
- The lack of proper community testing and ways for users and contributors to provide feedback, which would help identify and sustain the best or more promising resources
- The lack of a well-maintained, well-structured and simple-to-use catalogue to reference and locate these existing resources.

If we zoom in on the SOC operations, digital forensics, incident response and cyber threat intelligence activities alone, it is becoming increasingly difficult to identify which combination of tools, rules and playbooks one should integrate into existing operations, let alone build a detection and response capability from scratch.

While there are well-known products and tools that are not too difficult to identify by cybersecurity professionals, there are countless smaller pieces of software and tools that could be used to perform specific or infrequent tasks or to protect against new threats.

Analytics and detection rules, built using SIGMA, YARA or other formats, are another overwhelming maze in which one can easily get lost. Which clever insights has the community developed to find adversarial behaviour? Which detection rules are more relevant for my context? Which rules supersede or augment existing ones? Which authors tend to make more relevant rules for my environment? How do I identify duplicates in sets coming from various sources and avoid overloading my detection systems?

We find a similar situation when looking closely at playbooks and processes that the community is documenting in Jupyter notebooks or similar tools. What are the recommended steps I should perform to triage or contain a cyberattack? What are the best practices in incident response timelining? What are the processes my peers rely on that I can replicate in my environment?

All these questions are valid and, if not properly addressed, the cybersecurity community will keep losing precious time and reinventing the wheel at scale in an era where we can no longer afford this. In many cases, we have tools and frameworks available but locating, correlating, checking and maintaining them remain serious challenges. We believe that resolving these challenges and amplifying the impact of the combined knowledge of the community could be fostered by a well-structured, simple-to-use system as proposed in this White Paper.

We propose a system based on a taxonomy of well-defined namespaces for identifiers related to cybersecurity resources. While embryonic in its first iteration and there is certainly room for improvement, the taxonomy is extensible to cover future domains while being flexible to iron out defects and integrate improvements as the system’s adoption grows. The proposed system allows contextualisation to facilitate searching and selection using tags. As a decentralised structure, it allows authors to control the documentation and distribution of their content.

The system is designed in such a way that it is easy for organisations and individuals alike to obtain their unique namespaces, make and maintain entries in the catalogue corresponding to the resources they create. Essential features such as version control, crowd sourced vetting and quality control as well as deprecation will be integrated from the outset.

Finally, the system will, in a future iteration, facilitate interlinking resources that could be used in conjunction for an improved capability in coherent “packages”. Such “packages'' could then be deployed by less mature entities as plug-and-play solutions to save time and defend themselves properly, while avoiding the pitfalls resolved by early adopters or more mature organisations.

# The universal CYbersecurity resource CATalogue (CyCAT.org)

CyCAT.org or the Universal Cybersecurity Resource Catalogue aims at mapping and documenting, in a single formalism and catalogue all the community cybersecurity tools, rules, playbooks, processes and controls. CyCAT.org is positioned as a readily accessible catalogue for and by the community, distributed and non-commercial. Some level of moderation will be organised to assure the quality and reliability of the content.

Building on the success of existing initiatives such as CVE for vulnerabilities and elegant solutions such as the UUID used by MISP to uniquely identify and link events (e.g. which events extend or share attributes with one another), CyCAT.org provides mechanisms to programmatically attribute a unique identifier to:


- Cybersecurity tools
- Rules and rule sets (such as Sigma, YARA, Snort/Zeek/Suricata)
- Fingerprinting rules (such as ja3, jarm)
- Playbooks
- Notebooks
- Taxonomies
- Vulnerabilities
- Proof-of-concepts to validate such vulnerabilities
- Data models (MISP Objects, STIX extension)
- Mitigating controls

By making an API call, authors can reserve a unique identifier for their contributions, while providing simple metadata to describe their entry in the catalogue.

CYCAT will also provide a simple way for authors and contributors to suggest updates to the metadata of the entries in the library, flag links, overlaps between them, etc.

In addition, authors can query the library to identify whether the problem they are trying to tackle has already been solved elsewhere and avoid, if they so prefer, duplication of work.

CYCAT will offer users a web UI to query its content as well as CLI tools and API endpoints to interact with it and tag content that they are currently using or would like to experiment with in the future to have a holistic view of what they are using at a certain point in time in their operations, which rules, TTPs of IOC collections should be deprecated or replaced, which tools should be superseded by new ones, etc.

The aim is not to replace any existing initiative in cybersecurity but to link and offer better visibility to all project owners and user communities. CYCAT is a non-profit initiative runs by a team of motivated people to catalogue and crosslink cybersecurity resources.

# Intended Outcome

The purpose is to provide contributors a unique and simple way to document, contextualise, validate and cross-reference their contributions, taking into account and building upon prior art. For users the purpose is to facilitate searching, identifying and locating cybersecurity resources of relevance for a specific or broader purpose.

An example of the use of CYCAT in the current context would be to support pulling together the supply and demand for community insight, tools, rules and controls developed and made available to protect, detect and respond to threats such as the SolarWinds supply-chain attack. It would also provide an overview where they fit in the global view, like to which MITRE ATT&CK® (sub)techniques they are linked. Applying a rule from a ruleset in a network intrusion detection system can impact other elements in your organisation. CYCAT would also help to show where the rule fits within context.

# CyCAT.org Resources

- GitHub repository: [https://github.com/cycat-project](https://github.com/cycat-project)
- Website:  [https://www.cycat.org/](https://www.cycat.org/)
- Contributing via GitHub issues: [https://github.com/CyCat-project/cycat-project-website/issues](https://github.com/CyCat-project/cycat-project-website/issues)

# Timing

Initial feedback and peer review of the concept (White Paper and draft taxonomy) is expected between 1 February 2021 and 31 March 2021. The alpha version of the system is planned to be launched on the occasion of the next EU ATT&CK Community workshop on 1 June 2021.

# How to Submit Feedback?

The CyCAT.org project is in an initial phase and actively look for feedback.

# Who is Behind CyCAT.org?

We are four experienced, community-oriented cybersecurity professionals who have at heart to help our fellow defenders keep threats at bay while making their life simpler.

[Meet the team!](/team/)

