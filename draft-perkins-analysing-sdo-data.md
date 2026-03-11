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


   This document outlines a framework for measuring Internet standards
   development in the IETF and its relationship with other related standard 
   development organisations standards development
   organizations (SDOs). It identifies observable components of
   standards development processes, proposes a taxonomy of possible
   measurements, and discusses methodological, interpretive, and ethical
   considerations.

   The framework is intended to support a range of uses, including
   understanding technology deployment, monitoring SDOs, evaluating 
   the evolution of technical work, and informing community, leadership,
   and governance discussions.



--- middle

# Introduction

   Internet technologies are developed through a range of standards
   development organizations (SDOs), including organizations such as
   the IETF, W3C, IEEE, 3GPP, ITU-T, and others.

   These processes underpin the interoperability and architectural
   evolution of the Internet and the Web. Understanding how standards are 
   developed, including participation, collaboration, governance, and 
   technical outputs, can  can help to  monitor
   standards development organizations, understanding technology
   evolution and deployment, evaluating the evolution of technical work, and informing
   the community and its leadership, civil society and policy makers, as well as researchers from a wide range of disciplines.

   This document outlines a framework for measuring such systems.

   Goals:

   * Identify observable components of standards ecosystems
   * Provide a taxonomy of possible measurements
   * Highlight methodological considerations and limitations
   * Encourage reproducible measurement and analysis

   This document does not prescribe metrics or evaluation methods.




# Goals of Analysing Standards Data



# Data Availability

Standards development processes can be modeled as socio-technical
   systems composed of interacting elements.


   Key components include:

   Participants: 
      Individual contributors including engineers, operators,
      researchers, and independent contributors.
	

   Organizations: 
      Organizations (companies, academic institutions, civil society organizations,
      and governments associated) that participants are affiliated with.


   Technical Groups:
      Working groups, task forces, committees, or other technical bodies
      responsible for developing specifications.

   Artifacts:
      Technical documents such as drafts, specifications,
      recommendations, revisions, and related materials.

   Communication Infrastructure:
      Mailing lists, repositories, issue trackers, meetings, and
      collaborative platforms.

   Governance Structures:
      Review processes, editorial roles, leadership positions,
      consensus mechanisms, and decision-making processes.

Information on each of these components is available or can be partially inferred through different sources  discussed below.



## IETF Data Tracker

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

## RFC Editor

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

# Interpretation and Limitations: Governance, Power, and Culture

   Standards development processes involve both formal and informal
   governance structures, cultural norms and relationships of relative power.

   Measurement may consider:

   * Distribution of leadership roles (chairs, editors)
   * Concentration of authorship or editorial control
   * Organizational representation
   * Participation inequality

   There is in fact a wide range of aspects that these metrics are unlikely to capture influence, authority, or cultural aspects.
   A range of techniques including graph theory and natural languaje processing can help extract additional information from the existing data but in manyy cases alternative data sources such as interviews and survey will be necessary.


# Cross-SDO Ecosystems


   Internet technologies are frequently developed across multiple
   standards organizations.
   Different SDOs may focus on different layers of the technology stack
   or different aspects of a system. This document has so far focused on the IETF, we now consider its relationship in the broader context of INternet SDOs.
   Particularly relevant to the Internet and the IETF are W3C, ITU-T, and 3GPP.

   Measurement can therefore extend beyond a single organization to
   examine broader standards ecosystems.

   Examples of cross-SDO measurements include:

   * Overlap of participants across organizations
   * Organizational participation across multiple SDOs
   * Cross-references between technical specifications
   * Dependency relationships between standards produced in
     different organizations
   * Liaison relationships and coordination mechanisms

   Cross-SDO analysis can help identify ecosystem structures,
   collaboration patterns, dependencies across standards bodies, strategic behavior by standard developers.
   
   A broader perspective that takes into account an even wider ecosystem could consider other forums including policy oriented ones such as IGF as well as operational ones like Regional Registries, Network operator lists (NOGs) and ICANN.
   The goal of this document is not to cover any of these in detail but to highlight that a comprehensive understanding is possible and that data is available.


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
