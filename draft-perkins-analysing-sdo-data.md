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

The W3C...

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


The W3C...


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

TODO complete (there are more for sure...)

# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
