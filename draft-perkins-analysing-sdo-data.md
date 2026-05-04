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

 -
    fullname: Ignacio Castro
    organization: Queen Mary University of London
    email: i.castro@qmul.ac.uk

 -
    fullname: Ryo Yanagida
    organization: University of St Andrews
    email: ryo@htonl.net

normative:

informative:

...

--- abstract

This document outlines some issues to consider when studying data relating
to the Internet standards development ecosystem. It identifies observable
components of standards development processes, proposes a taxonomy of
possible measurements, and highlights methodological, interpretive, and
ethical considerations.  It is intended to support a range of uses,
including monitoring standards development organisations (SDOs), evaluating
the evolution of technical work, understanding technology deployment, and
informing community, leadership, and governance discussions.

This document is submitted for consideration by the Research and Analysis
of Standard-Setting Processes Research Group (RASPRG) in the IRTF.  It is
not an IETF product and is not a standard.


--- middle

# Introduction

Internet technologies are developed and standardised by a range of standards
development organisations (SDOs), including the IETF, W3C, IEEE,
3GPP, ITU-T, and others. The standards that these organisations produce underpin the interoperability
and architectural evolution of the Internet and the Web.

Understanding how standards are developed, including who participates in
the standards process, what collaborations occur during the development of
standards, how the process is organised and governed, and the technical
outputs, can support analysis of standards ecosystems. Such analysis can
assist with monitoring standards development organisations, evaluating the
evolution of technical work, understanding technology deployment, and
ultimately be used to inform community leadership and governance
discussions.

This document outlines considerations for studying data from the Internet
standards development ecosystem.  It first describes generic concepts and measurement
approaches that can be applied to standards development processes
in general. It then considers the IETF,
given the availability of rich data about its
participants, documents, processes, and communication channels.
Finally, it discusses how these approaches may apply to other SDOs,
and the extent to which differences in governance, transparency, and
data availability affect such analysis.


# Goals of Analysing Standards Data

This document aims to:

  * Identify the observable components of standards development ecosystems
  * Describe considerations for measuring and analysing standards
    development processes
  * Provide a taxonomy of possible measurements and analytical approaches
  * Highlight methodological, interpretive, and ethical considerations
  * Illustrate the application of these methods using the IETF
  * Discuss the relevance and limits of applying these methods to
    other SDOs
  * Encourage reproducible research practices and transparent analysis

This document does not prescribe specific metrics, define evaluation
criteria, or recommend comparative rankings of standards bodies,
groups, or participants.

# Standards Development as a Socio-Technical System

Internet standards development can be understood as a socio-technical
system in which technical artefacts, human participants, organisational
interests, and governance processes interact over time. Standards do not
emerge solely from technical design choices, nor solely from institutional
processes; rather, they arise through structured collaboration among
individuals and organisations operating within formal and informal rules.

Technical outputs emerge from a socio-technical process in which
engineering choices interact with expertise, incentives, organisational
structures, review processes, historical precedent, deployment
constraints, and the cultural norms and practices of the standards
community. At the same time, the organisational and cultural context is not fixed:
governance structures, working practices, and community norms
evolve together over time and these changes in turn shape future
participation and technical decision-making.

For analytical purposes, standards development ecosystems can be viewed
as comprising several interacting components:

* **Participants:**
  Participants are the individuals who contribute to standards development.
  They may include engineers, researchers, operators, implementers,
  academics, independent contributors, civil society representatives,
  policy specialists, and others with relevant expertise or interests.
  Participation criteria differ across SDOs.  Some use open participation,
  while others structure participation through organisational- or
  state-based membership, sometimes with additional exceptions or parallel
  open mechanisms.

  Participation models affect standards development by shaping both who is
  able to contribute, and how they are permitted to contribute. Open
  participation can broaden the pool of contributors and make it easier for
  individuals to join without prior institutional affiliation, which may
  increase diversity of experience and viewpoints. At the same time,
  openness does not eliminate all the barriers to participation. Effective
  participation may still depend on having sufficient time, funding,
  employer support, travel resources, and familiarity with the processes,
  tools, and norms of the community.  Membership-based models may provide
  clearer institutional commitment and resourcing, but they can also limit
  participation to those acting through recognised organisations or
  membership categories.


* **Organisations:**
  Participants are often affiliated with organisations such as companies,
  academic institutions, governments, consultancies, or civil society
  groups.  These organisations may provide forms of support including
  funding, staff time, technical expertise, or implementation experience.

  The relationship between participants and organisations is not equally
  visible across SDOs. In some models, participation is individual, and so
  any recorded affiliation may be incomplete, and reflect a specific
  contribution rather than the sustained view of the participant. In other
  models, where individuals participate on behalf of a clearly indicated
  affiliation, the institutional link is clearer.

  Even where affiliations are recorded, they may not fully describe the
  organisational context. A company may be a subsidiary of another company
  (or in the process of becoming so), and consultants or contractors may
  work for clients whose interests are not directly visible in
  participation records.


* **Technical Groups:**
  SDOs typically organise work through technical groups such as working
  groups, research groups, study group, committees, or similar bodies.
  These groups define scope, coordinate discussion, and develop technical
  outputs.  They are not always organised as a single flat layer, with
  hierarchical and other structures in use.

  The number, names, and functions of these structures differ across
  organisations. In some cases, they reflect administrative oversight or
  broad technical areas; in others, they distinguish between different
  forms of technical development.


* **Artefacts:**
  Standards processes generate artefacts such as drafts, specifications,
  recommendations, reports, agendas, minutes, presentations, issue
  trackers, and final published standards.  These artefacts provide an
  observable record of technical development.  Revision histories,
  references, and relationships between documents may help reveal aspects
  such as participation dynamics, design iteration, and the evolution of
  the underlying technologies subject to standardisation.

  Different SDOs vary in how openly they make such information available
  and in how easily it can be accessed and reused. artefact availability
  can support the work of participants, researchers, and other observers,
  but collecting, maintaining, publishing, and organising this information
  also imposes costs on SDOs.


* **Collaboration Infrastructure:**
  Standards development requires communication among participants to
  propose work, discuss technical issues, review contributions, coordinate
  activity, resolve disagreements, and build support for possible outcomes.
  SDOs therefore rely on systems such as mailing lists, code repositories,
  and meetings to facilitate this debate.

  The mix of communication, collaboration, and coordination mechanisms
  differs across SDOs, often to support the other attributes described.


* **Governance Structures:**
  Standards bodies have formal governance structures, with charters
  specifying the scope of different activities, defined leadership roles,
  review and approval stages, appeals processes, voting rules, consensus
  procedures, and so on. These structures define how work is initiated,
  scoped, reviewed, approved, and contested.

  At the same time, influence is also exercised  through reputation,
  recognised expertise, community norms, procedural familiarity, and
  control over agendas, drafting, or review capacity.  Governance
  structures therefore shape how decisions are made, how priorities are
  established, how disagreements are managed, and, ultimately, how
  influence is distributed within standards development.


* **Standards Implementation and Deployment:**
  Implementation usually occurs outside the formal standards process, and
  may be voluntary by interested parties or mandated by policy in certain
  jurisdictions.

  In many cases, publication of a standard does not by itself require
  implementation. Adoption may therefore vary widely: some standards are
  widely deployed, while others see limited or no implementation. Adoption
  may also be shaped by factors outside the standards process, including
  regulation, procurement, cost, and compatibility with existing systems.

  Data on implementation and operational use is often limited.


Measuring SDO activity is challenging. Observable metrics such as
publication counts, message volume, attendance figures, authorship, or
leadership roles can provide useful evidence, but each captures only
part of the standards process. Analysis of artefacts and logs from the
collaboration infrastructure (e.g., analysis of mailing list messages)
can provide more detail and nuance, at the expense of additional
complexity, but even these do not provide a complete view.

There are several reasons for this.
One is that critical aspects of standards development are
hard to observe directly. Influence, agenda setting, informal
coordination, negotiation, and the practical exercise of power and authority
may not be well represented by any single metric, or group of metrics, and
are extremely challenging to infer from collaboration infrastructure logs.

Another reason is that the available data is often limited. Data
availability and quality vary across SDOs. Different parts of the
process are not equally observable, and even within a single SDO some
information may be incomplete, difficult to access, inconsistently
structured, or unavailable.

Combining multiple data sources introduces additional challenges.
Observations from different parts of the process may not share stable
identifiers, identifiers may change over time, and the same entity may
appear in different forms across records. Voluntary declarations,
non-standard terminology, and organisational changes such as mergers or
acquisitions may further complicate linkage.

Metrics, artefacts, and other data sources may also differ in accuracy, representativeness, and
relevance. Not all artefacts have the same significance, not all forms
of participation have the same effect, and visible activity does not
necessarily correspond to implementation, adoption, or wider impact.
Measures should therefore be interpreted cautiously and, where
possible, considered alongside complementary indicators.



# Analysing the IETF

IETF participation is open with no formal
membership. Individuals can participate by joining mailing lists,
contributing to discussions, submitting Internet-Drafts, and attending
meetings. Contributions ordinarily reflect the opinion of individual participants, and
not necessarily their affiliation; exceptions to this norm exist for specific aspects
such as draft authorship and intellectual property rights disclosures.

The IETF has a hierarchical group structure, with technical working groups (that have working
group chairs) organised into distinct areas (that have area directors).

## Data Availability

Reflecting its open participation model, much of
the IETF's processes are publicly observable through open records and dedicated APIs. Mailing lists
are a central forum for working group discussion, alongside meetings; some groups also use
externally hosted repositories, for example on GitHub, to support
drafting and issue discussion.

### Datatracker

The IETF Datatracker (https://datatracker.ietf.org/) is the main source of
day-to-day and historical data about the operation of the IETF. It can be
accessed via the website or programmatically using a REST API and provides information about:

* People including names, email addresses, pronouns,
  biography, and photo, and external resources such as personal websites,
  GitHub usernames, and Orcid identifiers. The Datatracker maintains a
  record of the different names and email addresses used by individuals.

* Documents such as RFCs, Internet-drafts, agendas, blue
  sheets, working group charters, conflict reviews, shepherd write-ups,
  liaison statements, minutes, and presentation slides, including:

  * Metadata such as the title, name ("draft-ietf-..."), revision,
    date, state, and where appropriate abstract, working group, RFC number
    and publication stream, status on the standards track, area director,
    and document shepherd.

  * Submissions (e.g., different revisions of internet-drafts)
    with document name, revision, date, title, abstract, authors, group,
    and metadata about documents the submission replaces.

  * Authors with email address, affiliation, and country.

  * Events such as state changes state, expiration, details of
    IESG processing, IETF last call, directorate reviews, IANA reviews,
    etc., with the document name, revision, date, and responsible person.

  * Relationships including normative and informative references,
    and document replaced, updated, or obsoleted.

* Working groups, research groups, area, directorates,
  and leadership bodies such as the IESG, IRSG, and IAB, including the
  group name and acronym, group state, relationships between groups (e.g.,
  working groups are organised in areas), the mailing list, charter text,
  milestones, and who occupies key roles in the group.

* IESG processing, including ballot positions, the text
  of comments and discusses, and scheduling of the IESG review.

* Directorate membership and directorate reviews,
  including the document, reviewer, outcome, data, and the review text.

* Meetings, including both plenary and interim meetings,
  with venues, dates, and times, details of what groups met in what
  time slots, and registration and attendance data.

* IPR disclosures including the document that the IPR
  relates to, the person making disclosure, details of the patent, and
  licensing terms.

The Datatracker has been developed over time, and this is reflected in the data that is
available, with more recent data being significantly more complete than earlier data.
Datatracker profiles are only required for a subset of IETF activities (e.g., draft submission,
meeting registration), and so a number of active participants do not have a profile.

### RFC Editor

The RFC Editor makes the RFC index available in machine readable form at
https://www.rfc-editor.org/rfc-index.xml. The RFC index includes title,
authors, publication date, status, abstract, publication stream, name of
the precursor Internet-draft, and the IETF area and working group that
developed the RFC, if appropriate. This information is also available
in the IETF Datatracker.

Information about RFC errata is available on the RFC Editor website at
https://www.rfc-editor.org/errata.php. This data is also available in
machine readable form.



## Mailing List Archives

The IETF maintains public mail archives at https://mailarchive.ietf.org/
that are also available in machine readable form via IMAP from
imap.ietf.org. The recent mail archives are essentially complete, but some
historical lists that were not originally hosted on ietf.org are missing.
Spam emails have largely, but not entirely, been removed from the archive.
As of March 2026, the IETF mail archive contains approximately 3 million
messages from almost 1400 mailing lists, around 40GB of data, with some
messages dating back to the late 1980s.

The are significant data quality problems with older messages in the IETF
mail archive, due to problems with the original messages rather than the
archive, that make them difficult to process without significant clean-up.

## Session Recordings

The IETF makes video recordings of its plenary meetings available on
YouTube (https://www.youtube.com/user/ietf). Audio recordings of IETF
sessions from IETF 49 through to IETF 106 are available at
https://get.ietf.org/archive/audio.

## Chat Archives

The IETF makes chat logs available. Jabber was used prior to 2021, with
archives at https://get.ietf.org/archive/jabber/. More recently, Zulip
has been used accessible at zulip.ietf.org.


## GitHub

Some IETF working groups, and some individuals, make extensive use of
GitHub for document development and issue tracking. The IETF does not
maintain a complete list of GitHub repositories associated with its
work. The IETF Datatracker contains pointers to some repositories.

Using an appropriate GitHub API access, the following information
are available from Github:

* Information about users contributing through Github (Username,
  email address, and etc.)

* Contributions those users make directly to the document via
  commits

* Discourse through comments and issues

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

# Analysing Other SDOs

Standardization efforts happen across an array of SDOs and therefore a comprehensive analysis requires
covering multiple such SDOs. Each SDO brings its own peculiarities and challenges. An additional
and important challenge is the integration of data across multiple SDOs to understand the standardization landscape.
In this section we discuss several such SDOs with a specific focus in W3C and the challenges of data integration across the IETF and W3C.

## W3C

### The W3C API

The W3C provides API endpoints providing access to a range of information
available. The overview of the API can be found at https://www.w3.org/api/
and their endpoints are available at https://api.w3.org/doc.
The information available in the API includes:

* Information about documents, such as ID, date, URI, title, status,
  document types (recommendation, and etc.), and its version.

* Information about participants, such as their names, and affiliations

* Information about affiliations, such as their name, and their member
  status.

* Information about groups, such as name, participants in the group,
  chair, charter and etc.

This might seem similar to the IETF Datatracker in some aspects, however
there are a numerous differences in terms of process, structure, and etc.
such that they are not necessarily directly comparable to one another.

### W3C Mailing List Archive

The W3C maintains public mail archives at https://lists.w3.org/Archives/Public/
These are available as HTML renders of emails.

### Other sources

The W3C participants are active on GitHub as well. The information
related to those repositories can be gathered using the GitHub APIs.

## Integrating data across SDOs



# Recommendations

## for the IETF
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

## for the Researchers
* Work with a snapshot of the data instead of working with the live data

* Engage with the community (the picture you get from the data and analysis are often incomplete)

* Contribute the effort put into cleaning the data back to the IETF (potentially?)

* As per the Ethics and Data Protection section, be cautious about the
  implication of the outcomes.

TODO complete (there are more for sure...)

# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
