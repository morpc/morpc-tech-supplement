# MORPC Data & Mapping Technical Supplement

## Introduction
This document is intended to provide technical details and interpretation guidance common to data products created by the Mid-Ohio Regional Planning Commission (MORPC) Data & Mapping department.  It is intended primarily to capture details that are helpful for interpretation of data and visualizations included in MORPC reports but which could not be included in the report itself due to space constraints, clarity concerns, and the like.  It is intended primarily for technical audiences who are interested in better understanding the nuances of the data.  This is a living document, and both the content and organization are expected to change frequently.  It is expected that the content will not be highly structured at first and that additional structure will be added as the content volume grows.  This document is being developed incrementally as the need for content arises and as staff capacity allows.  If the reader finds that a topic of concern is not addressed here, or if they require additional clarification beyond what is provided in this document, they are encouraged to contact the Data & Mapping team at [dataandmaps@morpc.org](mailto:dataandmaps@morpc.org). In addition to this generally-applicable documentation, we strive to create detailed context-specific documentation for each data product we create, and such documentation exists for many of our data products.  Sometimes a link to the context-specific documentation accompanies the data.  If the link is not provided, readers are encouraged to reach out to the Data & Mapping team to request access to the documentation.  

## Variable/concept definitions

This section includes guidance useful for understanding what we mean when we refer to a specific variable or concept.  We try to be consistent in our usage of these terms, however sometimes circumstances for us to assign different meanings from what is listed below.  Be sure to read the text that accompanies the data and note any divergence from these definitions.  The terms are organized in alphabetical order.

### Employment/employed/unemployed

When we refer to employment, we are typically referring to persons who have a job (i.e. "employed) or who are actively seeking to have a job (i.e. "unemployed").  In constrast to the term "jobs" (see below), which refers to people in the place where they work, employment typically refers to the person in the place where they live.  The collection of people who are employed and unemployed is referred to as the "labor force".  Persons who do not have a job and who are not seeking to have a job are not included in the labor force. Typically, we account for persons in the labor force, both employed and unemployed, using data from the Bureau of Labor Statistics [Local Area Unemployment Statistics](https://www.bls.gov/lau/) (LAUS).  The data included in LAUS come from a regular Census Bureau survey of U.S. households called the [Current Population Survey](https://www.census.gov/programs-surveys/cps.html)

Another common source of employment information is the Census Bureau's [American Community Survey](https://www.census.gov/programs-surveys/acs/).  There are several tables which are useful for capturing the employment details of persons at their place of residence, and these tables are [summarized nicely on the Census Reporter website](https://censusreporter.org/topics/employment/).

### Jobs

When we refer to jobs, we are typically referring to an employed person (a.k.a. worker) in the location where they work.  Contrast this with "employment" (see above), which also refers to workers, but typically in the location where they live.  Workers usually include people who work for employers and those who are self-employed.  Typically, we account for people who work for employers using data from the Bureau of Labor Statistics [Quarterly Census of Employment and Wages](https://www.bls.gov/cew/) (QCEW), which includes workers who are covered by unemployment insurance. This is thought to [account for more than 95%](https://www.bls.gov/cew/) of U.S. jobs as of 2026.  More details about workers covered by QCEW is available [here](https://www.bls.gov/cew/overview.htm#coverage), and specific exclusions are available [here](https://www.bls.gov/cew/publications/employment-and-wages-annual-averages/current/home.htm#exclusions).  

A notable exclusion from QCEW data is self-employed workers.  In most cases we attempt to account for self-employed workers by scaling the QCEW-covered jobs by a factor based on the share of self-employed workers for the geography of interest.  For example, if it is estimated that 10% of the workers in an area are self-employed, we divide the QCEW by 0.9 (i.e. multiply by 1.11111) to estimate the total number of jobs.  Typically we infer the share of self-employed workers from U.S. Census Bureau data from the [American Community Survey](https://www.census.gov/programs-surveys/acs/), table [B24070](https://data.census.gov/table/ACSDT1Y2024.C24070).

One important caveat is that we typically do not include vacant jobs in our estimates - that is, jobs which exist but in which no worker is employed.

## Topics

This section contains structured content for topics that lend themselves to classification.  We will add structured discussion of select topics here when appropriate.  If you don't find what you are looking for here, check the "Miscellaneous notes" section below.


## Miscellaneous notes

This section includes miscellaneous notes about a variety of topics.  We have tried to put related items in close proximity, however the data we work with often defies hierarchies.  The organization of this section is intentionally flat, however we will consider migrating content into hierarchical structures in the "Topics" section above in cases where this makes sense.

### Note 1 headline

Some text about note 1

### Note 2 headline

Some text about note 2
