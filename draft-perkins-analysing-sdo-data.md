---
title: "Analysing Internet Standards Development Organisation Data"
abbrev: "Analysing Internet Standards"
category: info

docname: draft-perkins-analysing-sdo-data-latest
submissiontype: IRTF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
#area: AREA
workgroup: RASPRG
keyword:
 - Scientometrics
 - Internet Standards Development
venue:
  group: RASPRG
  type: Research Group
  mail: rasprg@irtf.org
  github: "csperkins/draft-analysing-sdo-data"
  latest: "https://csperkins.github.io/draft-analysing-sdo-data/draft-perkins-analysing-sdo-data.html"

author:
 -
    fullname: Colin Perkins
    organization: University of Glasgow
    email: csp@csperkins.org

normative:

informative:

...

--- abstract

TODO Abstract


--- middle

# Introduction

TODO Introduction


# Goals of Analysing Standards Data



# Data Availability

## IETF Data Tracker

People

* Names
* Pronouns
* Biography and photo in some cases

Person Alias

* Mapping names to people

Person Event

* Not useful?


External Resources

* Website, GitHub profiles, Orcid, etc

Email addresses

* Mapped to people and documents


Documents

* Many different types
* Name, title, version, date, abstract, type,
* RFC number
* AD, Shepherd
* Group, stream, state
* Standard status

Document submissions

* Document name, version, date, title, abstract
* Authors
* Group
* Replaces

Document Events

* Person
* Document, version
* Date
* Event type

Document relations

* Replaces, updates, cites, cited by, …

Document authors

* Document, person, email, affiliation, coumtry

IESG ballot positions and comments/discuss text

Groups

* Name, acronym, type, state, parent
* Mailing list
* Charter text
* AD

Group events

* Person, group, date, type, event

Group roles

* Chair, secretary, AD, …
* With history

Group milestones with history

Meetings

* Plenary and interim
* Venues, dates, Times
* Groups meeting in what slot

Meeting registration
Meeting attendance

IPR disclosures
* Person making disclosure
* Document
* Details of the disclosure

Directorate reviews
* Documents, reviewer, outcomes, dates, link to review text
* Membership of direcorates

Available email lists

## Session Recordings

## Mailing List Archives
Recent archives essentially complete
Some historical lists entirely missing
Significant data quality problems
* Don’t expect to throw the Python email parsing classes at them without
  significant cleanup

A significant number of the email addresses in the archive are not in the
data tracker.

## RFC Editor
RFC index
Errata

## GitHub

# Data Processing
Entity resolution is a significant challenge
* People
* Organisations

Affiliations are a significant challenge
* Dual affiliations

Document history is non-trivial

Role history is non trivial (e.g., who chaired what group when)
Group history is non trivial

Challenges with working with message contents

Incomplete or increasingly messy historical data

# Ethics and Data Protection

This is all personal data, subject to legal restrictions on processing in
many jurisdictions

Research will need ethics approval
* Results are potentially sensitive and need to be handled with care
* The data is public, but the implications of it are not always obvious
* e.g., one can derive measures of the effectiveness of individuals in
  certain roles that, if presented out of context, might be considered
  sensitive

Care with data access to avoid disruption to the standards process


# Recommendations

IETF can usefully spend effort to ensure all data is available from the
datatracker with a stable API

Spend effort on cleaning the data (e.g., event data is messy because the
format changes)

Backfill historical data where it is known correct

Where backfilled data is derived from primary sources, document provenance
(e.g., if using LLM to parse handwritten blue sheets to get authors names
and affiliations, scans of the original blue sheets must be retained and it
must be clear what is derived from them so the derived versions and be
checked and updated if necessary)
* There are examples where data has been incorrectly back filled

Process for corrections?

How to handle derived data?
* This is for researchers, not IETF

# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
