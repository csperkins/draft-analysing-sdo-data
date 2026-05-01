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

This document outlines a framework for measuring Internet standards
development ecosystems. It identifies observable components of
standards development processes, proposes a taxonomy of possible
measurements, and highlights methodological, interpretive, and ethical
considerations.

The framework is intended to support a range of uses, including
understanding technology deployment, monitoring standards development
organizations (SDOs), evaluating the evolution of technical work, and
informing community, leadership, and governance discussions.


--- middle

# Introduction

Internet technologies are developed through a range of standards
development organizations (SDOs), including the IETF, W3C, IEEE,
3GPP, ITU-T, and others. These processes underpin the interoperability
and architectural evolution of the Internet and the Web.

Understanding how standards are developed, including participation,
collaboration, governance, and technical outputs, can support analysis
of standards ecosystems. Such analysis can assist with monitoring
standards development organizations, understanding technology
deployment, evaluating the evolution of technical work, and informing
community leadership and governance discussions.

This document outlines considerations for studying data from the Internet
standards ecosystem.  It first describes generic concepts and measurement
approaches that can be applied to standards development processes
in general. It then considers the IETF as a detailed worked example,
since the IETF provides unusually rich public data about its
participants, documents, processes, and communication channels.
Finally, it discusses how these approaches may apply to other SDOs,
and the extent to which differences in governance, transparency, and
data availability affect such analysis.


# Goals of Analysing Standards Data

This document has the following goals:

  * Identify the observable components of standards development ecosystems
  * Describe a framework for measuring and analysing standards
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
community. At the same time, the organisational and cultural context is not fixed,
however: governance structures, working practices, and community norms
evolve together over time and these changes in turn shape future
participation and technical decision-making.

For analytical purposes, standards development ecosystems can be viewed
as comprising several interacting components.

## Participants

Participants are the individuals who contribute to standards
development. They may include engineers, researchers, operators,
implementers, academics, independent contributors, civil society
representatives, policy specialists, and others with relevant
expertise or interests.

Participation criteria differ across SDOs. Some use open participation,
while others structure participation through organisational or state-
based membership, sometimes with additional exceptions or parallel open
mechanisms. In the IETF, participation is open: there is no formal
membership, and individuals may participate by joining mailing lists,
contributing to discussions, submitting Internet-Drafts, and registering
for meetings. In W3C, by contrast, participation in formal groups is
generally through organisational membership, although non-members may in
some cases participate as Invited Experts and some groups, such as
Community Groups, are open without W3C Membership. In ITU-T,
participation is structured through membership categories, with Member
States participating directly and other entities, including companies,
organisations, and academic institutions, participating through the
relevant membership categories and the rights attached to them. These
differences are analytically relevant because they affect who can
participate, in what capacity, and under what conditions.

Participation models affect standards development by shaping who and how is
able to contribute. Open participation can broaden the pool of
contributors and make it easier for individuals to join without prior
institutional affiliation, which may increase diversity of experience
and viewpoints. At the same time, openness does not eliminate barriers
to participation. Effective participation may still depend on having
sufficient time, funding, employer support, travel resources, and
familiarity with the processes, tools, and norms of the community.
Membership-based models may provide clearer institutional commitment and
resourcing, but they can also limit participation to those acting
through recognised organisations or membership categories.


## Organisations

Participants are often affiliated with organisations such as companies,
academic institutions, governments, consultancies, or civil society
groups. These organisations may provide forms of support including funding, staff time, technical expertise, or implementation experience.

The relationship between participants and organisations is not equally
visible across SDOs. In open participation models such as the IETF,
participation is individual rather than membership-based, so any
recorded affiliation may be incomplete and it is declaration is voluntary (exceptions to this norm exist for specific aspects such as draft authorship and intellectual property rights disclosures). In membership-based models, the institutional link is clearer: for example, W3C participation in formal groups is generally through member
organisations, and ITU-T participation is structured through membership
categories and the rights associated with them.

Even where affiliations are recorded, they may not fully describe the
organisational context. A company may be a subsidiary of another
company (or in the process of becoming so), and consultants or contractors may work for  clients whose interests are not directly visible in participation records.


## Technical Groups

SDOs typically organise work through technical groups such as working
groups, research groups, committees, or similar bodies. These groups
define scope, coordinate discussion, and develop technical outputs.
They are not always organised as a single flat layer. In the IETF,
working groups are chartered within Areas. In ITU-T, the work is
centred on Study Groups, which may be structured into Working Parties,
with specific Questions assigned within that structure. In W3C, by
contrast, Working Groups, Interest Groups, and Coordination Groups are
different types of groups with different functions, rather than levels
in a single hierarchy.

The number, names, and functions of these structures differ across
organisations. In some cases, they reflect administrative oversight or
broad technical areas; in others, they distinguish between different
forms of technical development.



## Artifacts

Standards processes generate artifacts such as drafts,
specifications, recommendations, reports, agendas, minutes,
presentations, issue trackers, and final published standards.
These artifacts provide an observable record of technical development.
Revision histories, references, and relationships between documents may
help reveal aspects such as participation dynamics, design iteration, a
nd the evolution of the underlying technoilogies subject to standardisation.

Different SDOs vary in how openly they make such information available
and in how easily it can be accessed and reused. In the IETF, much of
the standards process is publicly observable through open records and dedicated APIs.
In W3C, some information is public, including charters for chartered groups,
while other material may be limited to Members or specific participants depending on the
group and the status of its proceedings. In ITU-T, document access is
structured by document category, with some material made publicly
available, including Recommendations, and other material available only
to members through member services. Articfact availability can support the
work of participants, researchers, and other observers, but collecting,
maintaining, publishing, and organising this information also imposes
costs on SDOs.

## 2.5. Communication Infrastructure

Standards development requires communication among participants to
propose work, discuss technical issues, review contributions,
coordinate activity, resolve disagreements, and build support for
possible outcomes. SDOs therefore rely on systems such as mailing
lists, code repositories, and meetings.

The mix of communication, collaboration, and coordination mechanisms
differs across SDOs. In the IETF, mailing lists are a central forum for
working group discussion, alongside meetings; some groups also use
externally hosted repositories, for example on GitHub, to support
drafting and issue discussion. In W3C, communication commonly takes
place through repositories and issue trackers, meetings and
teleconferences, and, depending on the group, mailing lists and chat
channels. In ITU-T, communication takes place through meetings,
mailing lists, and formal liaison statements, while contributions and
other working documents are circulated through member-access document
services.

## Governance Structures

Standards bodies typically operate through formal governance
structures, such as charters, defined leadership roles, review and
approval stages, appeals processes, voting rules, or consensus
procedures. These structures define how work is initiated, scoped,
reviewed, approved, and contested.

At the same time, governance is also exercised  through reputation, recognised expertise, community norms, procedural
familiarity, and control over agendas, drafting, or review capacity.
Governance structures therefore shape how decisions are made,
 how priorities are established, how disagreements are managed,
and, ultimately, how influence is distributed within standards development.

## External Deployment Ecosystem

Implementation usually occurs outside the formal standards process.
Many Internet related standards such as those developed by  the IETF, W3C, and ITU-T,
publication does not by itself require implementation. Adoption may
therefore vary widely: some standards are widely deployed, while others
see limited or no implementation. Adoption may also be shaped by
factors outside the standards process, including regulation,
procurement, cost, and compatibility with existing systems.

Data on implementation and operational use is often limited or
unavailable.


## Implications for Measurement

Measuring SDO activity is challenging. Observable metrics such as
publication counts, message volume, attendance figures, authorship, or
leadership roles can provide useful evidence, but each captures only
part of the standards process.

One reason is that critical aspects of standards development are
hard to observe directly. Influence, agenda setting, informal
coordination, negotiation, and the practical exercise of power and authority
may not be well represented by any single metric.

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

Metrics may also differ in accuracy, representativeness, and
relevance. Not all artifacts have the same significance, not all forms
of participation have the same effect, and visible activity does not
necessarily correspond to implementation, adoption, or wider impact.
Measures should therefore be interpreted cautiously and, where
possible, considered alongside complementary indicators.



# Analysing the IETF

## Data Availability

### Data Tracker

The IETF Data Tracker (https://datatracker.ietf.org/) is a major source of
day-to-day and historical data about the operation of the IETF. It can be
accessed via the website or programmatically using a REST API and provides:

* Information about people including names, email addresses, pronouns,
  biography, and photo, and external resources such as personal websites,
  GitHub usernames, Orcid identifiers, etc. The data tracker maintains a
  record of the different names and email addresses used by individuals.

* Information about documents such as RFCs, Internet-drafts, agendas, blue
  sheets, working group charters, conflict reviews, shepherd write-ups,
  liaison statements, minutes, presentation slides, etc., including:

  * Document metadata such as the title, name ("draft-ietf-..."), revision,
    date, state, and where appropriate abstract, working group, RFC number
    and publication stream, status on the standards track, area director,
    and document shepherd.

  * Document submissions (e.g., different revisions of internet-drafts)
    with document name, revision, date, title, abstract, authors, group,
    and metadata about documents the submission replaces.

  * Document authors with email address, affiliation, and country.

  * Document events such as state changes state, expiration, details of
    IESG processing, IETF last call, directorate reviews, IANA reviews,
    etc., with the document name, revision, date, and responsible person.

  * Document relations including normative and informative references,
    and document replaced, updated, or obsoleted.

* Information about working groups, research groups, area, directorates,
  and leadership bodies such as the IESG, IRSG, and IAB, including the
  group name and acronym, group state, relationships between groups (e.g.,
  working groups are organised in areas), the mailing list, charter text,
  milestones, and who occupies key roles in the group.

* Information about IESG processing, including ballot positions, the text
  of comments and discusses, and scheduling of the IESG review.

* Information about directorate membership and directorate reviews,
  including the document, reviewer, outcome, data, and the review text.

* Information about meetings, including both plenary and interim meetings,
  with venues, dates, and times, and details of what groups met in what
  time slots. Registration and attendance data.

* Information about IPR disclosures including the document that the IPR
  relates to, the person making disclosure, details of the patent, and
  licensing terms.

The data tracker has been developed piecemeal over time, and the data it
provides reflects that with more recent data being significantly more
complete than earlier data.

### RFC Editor

The RFC Editor makes the RFC index available in machine readable form at
https://www.rfc-editor.org/rfc-index.xml. The RFC index includes title,
authors, publication date, status, abstract, publication stream, name of
the precursor Internet-draft, and the IETF area and working group that
developed the RFC, if appropriate. This information is also available
in the IETF Data tracker.

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
work. The IETF data tracker contains pointers to some repositories.

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

The W3C participants are active on GitHub as well...

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
