# MORPC Data & Mapping Technical Supplement

## Introduction
This document is intended to provide technical details and interpretation guidance common to data products created by the Mid-Ohio Regional Planning Commission (MORPC) Data & Mapping department.  It is intended primarily to capture details that are helpful for interpretation of data and visualizations included in MORPC reports but which could not be included in the report itself due to space constraints, clarity concerns, and the like.  It is intended primarily for technical audiences who are interested in better understanding the nuances of the data.  This is a living document, and both the content and organization are expected to change frequently.  It is expected that the content will not be highly structured at first and that additional structure will be added as the content volume grows.  This document is being developed incrementally as the need for content arises and as staff capacity allows.  If the reader finds that a topic of concern is not addressed here, or if they require additional clarification beyond what is provided in this document, they are encouraged to contact the Data & Mapping team at [dataandmaps@morpc.org](mailto:dataandmaps@morpc.org). In addition to this generally-applicable documentation, we strive to create detailed context-specific documentation for each data product we create, and such documentation exists for many of our data products.  Sometimes a link to the context-specific documentation accompanies the data.  If the link is not provided, readers are encouraged to reach out to the Data & Mapping team to request access to the documentation.  

## Variable/concept definitions

This section includes guidance useful for understanding what we mean when we refer to a specific variable or concept.  We try to be consistent in our usage of these terms, however sometimes circumstances for us to assign different meanings from what is listed below.  Be sure to read the text that accompanies the data and note any divergence from these definitions.  The terms are organized in alphabetical order.


### Employment/employed/unemployed

When we refer to employment, we are typically referring to persons who have a job (i.e. "employed") or who are actively seeking to have a job (i.e. "unemployed").  In constrast to the term "jobs" (see below), which refers to people in the place where they work, employment typically refers to the person in the place where they live.  The collection of people who are employed and unemployed is referred to as the "labor force".  Persons who do not have a job and who are not seeking to have a job are not included in the labor force. Typically, we account for persons in the labor force, both employed and unemployed, using data from the Bureau of Labor Statistics [Local Area Unemployment Statistics](https://www.bls.gov/lau/) (LAUS).  The data included in LAUS come from a regular Census Bureau survey of U.S. households called the [Current Population Survey](https://www.census.gov/programs-surveys/cps.html)

Another common source of employment information is the Census Bureau's [American Community Survey](https://www.census.gov/programs-surveys/acs/).  There are several tables which are useful for capturing the employment details of persons at their place of residence, and these tables are [summarized nicely on the Census Reporter website](https://censusreporter.org/topics/employment/).


### Jobs

When we refer to jobs, we are typically referring to an employed person (a.k.a. worker) in the location where they work.  Contrast this with "employment" (see above), which also refers to workers, but typically in the location where they live.  Workers usually include people who work for employers and those who are self-employed.  Typically, we account for people who work for employers using data from the Bureau of Labor Statistics [Quarterly Census of Employment and Wages](https://www.bls.gov/cew/) (QCEW), which includes workers who are covered by unemployment insurance. This is thought to [account for more than 95%](https://www.bls.gov/cew/) of U.S. jobs as of 2026.  More details about workers covered by QCEW is available [here](https://www.bls.gov/cew/overview.htm#coverage), and specific exclusions are available [here](https://www.bls.gov/cew/publications/employment-and-wages-annual-averages/current/home.htm#exclusions).  

A notable exclusion from QCEW data is self-employed workers.  In most cases we attempt to account for self-employed workers by scaling the QCEW-covered jobs by a factor based on the share of self-employed workers for the geography of interest.  For example, if it is estimated that 10% of the workers in an area are self-employed, we divide the QCEW by 0.9 (i.e. multiply by 1.11111) to estimate the total number of jobs.  Typically we infer the share of self-employed workers from U.S. Census Bureau data from the [American Community Survey](https://www.census.gov/programs-surveys/acs/), table [B24070](https://data.census.gov/table/ACSDT1Y2024.C24070).

One important caveat is that we typically do not include vacant jobs in our estimates - that is, jobs which exist but in which no worker is employed.


### Sector, Industry, and Occupation
The terms *sector, industry,* and *occupation* are related but distinct concepts used to describe different dimensions of economic activity and labor markets.

In some contexts, “sector” may be used loosely to describe groupings such as public vs. private sector or goods-producing vs. service-providing industries. Any deviation from standard NAICS-based usage should be noted explicitly in the accompanying text.

Industry refers to the type of economic activity conducted by an establishment, based on what the business produces or the service it provides. Industry classifications in MORPC products typically follow the North American Industry Classification System (NAICS), a hierarchical system jointly developed by U.S., Canadian, and Mexican statistical agencies. NAICS allows industries to be analyzed at varying levels of detail (e.g., 2-digit sectors through 6-digit detailed industries). Industry-based data are commonly sourced from the Bureau of Labor Statistics Quarterly Census of Employment and Wages (QCEW), the U.S. Census Bureau County Business Patterns (CBP), and The American Community Survey (ACS).

Industry is frequently used to refer to high-level groupings that typically corresponding to the 2-digit NAICS level (e.g., Manufacturing, Health Care and Social Assistance). (NAICS codes are updated every 5-years, crosswalks are needed for converting between each 5-year period. [North American Industry Classification System - 2022](https://www.bls.gov/cew/classifications/industry/industry-titles.htm)

**[QCEW Data Files](https://www.bls.gov/cew/downloadable-data-files.htm)**

Occupation refers to the type of work performed by an individual worker, regardless of the industry in which they are employed. Occupational classifications typically follow the Standard Occupational Classification (SOC) system. Occupation-based data are most often derived from household surveys such as - The American Community Survey (ACS) Tables; **S2401** (Occupation), **S2405** (Industry by Occupation), **S2406** (Occupation by Class of Worker) - or the Current Population Survey (CPS). Because occupations are person-based rather than establishment-based, occupation data are generally tied to place of residence rather than place of work unless otherwise specified.

[Standard Occupational Classification and Coding Structure 2018](https://www.bls.gov/soc/2018/soc_2018_whats_new.pdf)
**[SOC - Occupational Employment and Wage Statistics](https://www.bls.gov/oes/tables.htm)**


### Inflation Adjustments

When working with variables expressed in dollar terms, MORPC will often adjust values for inflation to improve comparability across time. Unless otherwise noted, inflation-adjusted values should be interpreted as representing constant purchasing power rather than nominal dollars.

In most circumstances, dollar values are adjusted to the **most recent year available in the underlying dataset**, rather than the current calendar year. In some cases; such as long-term trend analyses or comparisons across multiple reports, values may be adjusted to a fixed reference year. The chosen inflation adjustment year will be explicitly stated in the primary document.

Inflation adjustments are calculated using the Bureau of Labor Statistics **Consumer Price Index for All Urban Consumers (CPI-U), U.S. City Average**, annual average, not seasonally adjusted. MORPC uses Series ID [**CUUR0000SA0**](https://data.bls.gov/pdq/SurveyOutputServlet), which has a base period of 1982–84 = 100. Annual averages are calculated by averaging the monthly CPI values for each year.

The general formula used is:
**Adjusted Dollar Value = Original Dollar Value × (CPI of target year ÷ CPI of original year)**

Because CPI represents average price changes across a broad basket of goods and services, inflation-adjusted values should be interpreted as approximations of purchasing power and not as precise cost-of-living measures for specific populations or regions.


### Federal Poverty Level (FPL)

The **Federal Poverty Level (FPL)** is the income threshold developed annually by the U.S. Department of Health and Human Services [Federal Poverty Guidelines](https://aspe.hhs.gov/topics/poverty-economic-mobility/poverty-guidelines) (HHS). This threshold varies based on household size; the larger the household size, the higher the household income can be for determining the households FPL.

The HHS poverty guidelines, or percentage multiples of them (eg: 50 percent, 100 percent, 125 percent, 150 percent, 185 percent, 200 percent, or 400 percent), are used as means-tested criterion to determin individuals or households eligibility for a number of state and federal programs. Program eligibility thresholds often exceed 100% FPL and may incorporate additional rules such as asset tests, categorical eligibility, or deductions. 

When income is expressed as a percentage of FPL,
1. The poverty level is calculated by dividing the household income by the stated income value for the family/household size that represents that year's Federal Poverty Level. A household making exactly the value for their household size for the federal poverty level would equal 100%, whereas a household income less than the FPL will be less than 100% and incomes above will be greater than.  
2. The value should be interpreted as a relative measure rather than a definitive indicator of economic hardship or self-sufficiency. 

MORPC frequently makes use of Ameircan Community Survey (ACS) tables that detail the Ratio of Income to Poverty Level in the Past 12 Months. These tables are in the B- & C-17 table sets, specifically: **C17002** (5-year estimates available, Universe: Population for whom poverty status is determined), **B17002** (1-year estimates only, Universe: Population for whom poverty status is determined), and **B17026** (1- & 5-year estimates available, Universe: Families).

### Housing Cost Burden

**Housing cost burden** refers to the share of a household’s income that is spent on housing-related costs. A household is typically considered *cost-burdened* if housing costs exceed **30% of gross household income**, and ***severely cost-burdened*** if housing costs exceed **50%**.

Housing costs generally include:
* For renters: gross rent (contract rent plus utilities)
* For homeowners: mortgage payments, property taxes, insurance, utilities, and selected fees

MORPC commonly relies on the U.S. Census Bureau’s American Community Survey (ACS) for housing cost burden estimates. These values are self-reported and reflect typical monthly expenses rather than exact accounting records. 
ACS Tables: **B25140** (by tenure), **B25106** (tenure by household income).

Housing cost burden is a useful screening metric but has limitations. It does not account for differences in household size, debt obligations outside of housing, or regional cost-of-living factors beyond housing. As a result, households with similar cost burden ratios may experience very different levels of financial stress.


### Home Sale Price to Income Ratio

The **home sale price to income ratio** is a measure of housing affordability for a defined region that compares the price of a home to the income of a typical household. It is generally calculated as:

**Ratio = Median Home Sale Price ÷ Median Household Income**

Higher ratios indicate reduced affordability, as households must devote a larger share of income to purchase a home. MORPC derives median home price from accessing the Central Ohio MLS data for real estate transactions and income data from the ACS.

Generally, a ratio that is less than 2.6 is considered "affordable", between 2.6 and 4 as "oderately unaffordable" and above 4 as "unaffordable".

This ratio is a simplified indicator and does not account for interest rates, down payment requirements, credit access, property taxes, insurance, or household composition. As such, it should be interpreted as a high-level comparative metric rather than a precise measure of homeownership feasibility.


### Education Attainment

Educational attainment refers to the highest level of education completed by an individual, typically measured for the population aged 25 and older. MORPC generally relies on the American Community Survey (ACS) for educational attainment data.
ACS Tables: **B15003**, **B15002 A-I**

Common educational attainment combined categories include:
* Less than a high school diploma or equivalent
* High school diploma, GED, or equivalent
* Some College
* Associate's degree and/or certification in a trade skill
* Bachelor's degree
* Post graduate degree (Masters, PhD, Professional Degree)

Educational attainment can be used to evaluate workforce skill levels, earnings potential, and access to economic opportunity. However, it does not capture credentials such as certifications, apprenticeships, or informal training, nor does it reflect field of study or quality of education.

### Race and Ethnicity

Race and ethnicity data used by MORPC is primarily drawn from two sources: The American Community Survey (table: **B03002**) and Census PEP (***SOURCE***). 
Race captures one or more categories such as White, Black or African American, Asian, American Indian or Alaska Native, Native Hawaiian or Other Pacific Islander, or Some Other Race. While ethnicity indicates whether a person is of Hispanic or Latino origin, regardless of race.

When reporting race and ethnicity, MORPC may present mutually exclusive categories (e.g., “Non-Hispanic White”), allow for multiracial identification, and/or different combinations of racial and ethicity demographics to make the tables or figures more easily digestible depending on analytical needs and data constraints. Small sample sizes, disclosure avoidance techniques, and category aggregation can affect the precision and comparability of race and ethnicity estimates, particularly for smaller geographies.

Race and ethnicity variables are social constructs and should be interpreted as reflecting self-identification rather than biological or genetic distinctions.

### Topics

This section contains structured content for topics that lend themselves to classification.  We will add structured discussion of select topics here when appropriate.  If you don't find what you are looking for here, check the "Miscellaneous notes" section below.


## Miscellaneous notes

This section includes miscellaneous notes about a variety of topics.  We have tried to put related items in close proximity, however the data we work with often defies hierarchies.  The organization of this section is intentionally flat, however we will consider migrating content into hierarchical structures in the "Topics" section above in cases where this makes sense.

### Note 1 headline

Some text about note 1

### Note 2 headline

Some text about note 2
