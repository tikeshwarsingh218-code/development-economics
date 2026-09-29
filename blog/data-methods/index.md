---
layout: default
title: Data and Methods
---

### Data and methods

Notes on the datasets and empirical tools that I use in research.

### Periodic Labour Force Survey

The Periodic Labour Force Survey is an important source for studying employment and labour market conditions in India. It provides information on labour force participation, employment, unemployment, workers, household characteristics, and different forms of economic activity. I use the survey to understand patterns in labour markets across individuals, households, and regions.

Working with PLFS requires more than simply opening the data and running regressions. The questionnaire, variable definitions, coding structure, missing values, sampling design, and survey weights all need to be understood before analysis. I therefore treat the documentation and structure of the survey as an important part of the empirical work.

### The redesigned PLFS from 2025

The redesigned PLFS introduced from 2025 provides a new framework for collecting and reporting information on labour market conditions in India. The changes are important for researchers because the frequency and organisation of the survey affect how labour market indicators can be studied over time.

The redesigned survey also requires care when comparing recent observations with earlier PLFS rounds. Changes in questionnaires, sampling procedures, definitions, and estimation methods can influence measured outcomes. Understanding these changes is necessary before making comparisons across different periods.

### Understanding the PLFS sampling design

Understanding the sampling design is an important part of working with household survey data. PLFS observations come from a structured sample rather than a simple random selection of individuals. The sample design determines how households enter the survey and how observations should be interpreted in relation to the wider population.

Sampling weights, strata, and sampling clusters can affect both estimates and statistical inference. I therefore try to understand how the sample was constructed before calculating population statistics or estimating relationships. This helps ensure that the empirical analysis reflects the design of the survey.

### Building an India district panel

An India district panel can be used to study economic and social changes across geographic areas over time. District level data can provide a useful way to examine differences in development, employment, public services, infrastructure, and other outcomes across regions.

Building such a panel is not simply a matter of combining files from different years. District boundaries and administrative structures change over time, and new districts are created from older ones. Constructing a consistent panel therefore requires careful geographic matching and documentation of the decisions used to connect observations across years.

### Matching districts across Census years

Districts in India have changed substantially across different Census periods. A district recorded in one Census may later be divided into several districts, merged with another area, or renamed. This creates difficulties when attempting to compare district level outcomes across different Census years.

I approach this as a geographic matching problem rather than relying only on district names. Historical boundaries, administrative changes, geographic locations, and other information can help determine how observations from different periods should be connected. Keeping the original identifiers is also important for checking the resulting matches.

### Constructing historical geographic crosswalks

Historical geographic crosswalks provide a way to connect geographic units that were defined differently at different points in time. They are particularly useful when combining datasets collected under different administrative boundaries. Without a crosswalk, apparently similar geographic observations may not actually represent the same area.

Constructing a crosswalk requires decisions about how older and newer geographic units overlap. Geographic boundaries, area relationships, and population information can all be useful depending on the research question. I also find it important to document the original geographic units and the procedures used to create the final relationship.

### Geocoding schools and administrative records

Many administrative datasets contain names and addresses but do not provide reliable geographic coordinates. Geocoding converts these descriptions into geographic locations that can be used for mapping and spatial analysis. This is particularly useful for schools, government offices, villages, and other public institutions.

Geocoding is also a data quality problem. A returned coordinate does not automatically mean that the observation has been correctly located. Names need to be standardised, possible matches need to be examined, and selected observations often need additional verification before the coordinates can be used confidently.

### Working with spatial data in R

R provides a useful environment for combining data cleaning with spatial analysis. Spatial data can be used to map observations, connect points to administrative boundaries, calculate distances, and examine geographic patterns. Keeping these operations within a coded workflow also makes the analysis easier to reproduce.

I use spatial workflows when research questions require information about where observations are located. Repeated geographic operations can be automated through code rather than performed manually for every dataset. This becomes especially useful when working with large numbers of schools, districts, villages, or administrative records.

### Working with QGIS

QGIS is useful for visually examining geographic data. Maps can reveal problems that may not be obvious when looking at a table of coordinates or administrative identifiers. Incorrect locations, unusual clusters, boundary problems, and unexpected geographic patterns can often be identified through visual inspection.

I see QGIS as complementary to statistical programming. Code is useful for performing the same operation systematically across a large dataset, while QGIS is useful for examining the results visually. Moving between the two can make spatial data cleaning and validation more reliable.

### Cleaning and standardising administrative data

Administrative data often contain substantial variation in names, formats, categories, and identifiers. The same institution, office, designation, or location can appear differently across different files. These differences can create problems when several administrative sources need to be combined.

I prefer to preserve the original values while creating standardised versions for analysis. This makes it possible to trace a cleaned observation back to its original form. Standardisation should make the dataset easier to analyse while keeping the cleaning process transparent and verifiable.

### Matching names across datasets

Matching names across datasets is often more difficult than it appears. Names may differ because of spelling, punctuation, abbreviations, spacing, transliteration, or changes in official terminology. Two records that look different may refer to the same entity, while similar names may refer to different entities.

I use a combination of standardisation, exact matching, approximate matching, and manual verification. Approximate matching can help identify possible matches, but it should generally be treated as a way of generating candidates rather than as final evidence. Additional information is often necessary to establish whether two records genuinely refer to the same entity.

### Working with messy government data

Government datasets can contain valuable information that would be difficult to collect independently. At the same time, these datasets may contain inconsistent formats, missing identifiers, duplicate observations, changing classifications, and limited documentation. Working with them therefore requires substantial attention before they can be used for empirical analysis.

I try to understand how the data were originally produced before making extensive changes to them. This includes examining the source, structure, definitions, identifiers, and patterns of missing information. The cleaning process should preserve enough information to explain how the original records were transformed into the final research dataset.

### Extracting information from PDFs

PDF documents often contain useful information that is not available in machine readable datasets. Government reports, administrative records, tables, lists, and historical documents may all need to be extracted before they can be used in quantitative research.

Extraction itself does not guarantee accurate data. Tables can be incorrectly read, scanned documents can produce recognition errors, and formatting can be lost during conversion. I therefore treat extracted information as an intermediate product that needs to be checked against the original document before being incorporated into a research dataset.

### Building analysis ready survey data

Survey data usually require substantial preparation before they can be used for analysis. Variables may have unclear names, different coding systems, missing value codes, multiple questionnaire versions, and derived measures that need to be constructed. Understanding the questionnaire is therefore an important part of understanding the dataset.

I treat cleaning as part of the research process rather than as a purely technical step. Decisions about missing observations, sample restrictions, variable construction, and coding can affect empirical results. Keeping these decisions documented makes the movement from raw survey data to analysis ready data easier to understand.

### Survey weights and complex survey design

Household surveys are generally designed to provide information about a wider population rather than only the people who were interviewed. Survey weights help account for the way observations were selected and allow researchers to produce estimates that correspond more closely to the population represented by the survey.

Weights are only one component of a complex survey design. Stratification and clustering can also affect estimation and standard errors. I therefore try to understand the complete survey design before deciding how a dataset should be analysed rather than treating the weight variable as an ordinary variable.

### Difference in Differences

Difference in Differences is a method for studying changes associated with an intervention or policy when some units are exposed to the intervention and others are not. The basic comparison considers how outcomes change over time for the treated group relative to the change experienced by a comparison group.

The credibility of the approach depends heavily on the research design. In particular, researchers need to think carefully about whether the comparison group provides a reasonable representation of what would have happened to the treated group without the intervention. Timing, pre intervention trends, anticipation, and other simultaneous changes can therefore be important.

### Randomized Controlled Trials

Randomized Controlled Trials use a random process to assign participants or other units to different groups. Random assignment is intended to create comparable groups before an intervention takes place. Differences in outcomes between the groups can then provide evidence about the effect of the intervention.

The statistical idea is only one part of an experiment. Recruitment, randomisation, treatment delivery, measurement, attrition, and survey implementation can all influence the quality of the final evidence. Careful preparation and monitoring during fieldwork are therefore essential parts of experimental research.

### Experimental research in development economics

Experimental research can be used to study whether specific interventions affect economic and social outcomes. In development economics, experiments have been used to examine questions involving education, employment, information, public services, financial decisions, health, and household behaviour.

I am particularly interested in the connection between the research question, intervention, and outcome being measured. An experiment requires decisions about who participates, how treatment is delivered, what information is collected, and how outcomes are measured. Good experimental research therefore combines economic reasoning with careful field implementation and empirical analysis.

### Survey design and questionnaire development

A questionnaire is the main instrument through which many research projects measure behaviour, beliefs, experiences, and outcomes. The wording of questions, order of sections, response options, and length of an interview can all affect the information respondents provide.

Questionnaire development therefore involves repeated testing and revision. Pilot interviews can reveal questions that respondents interpret differently from what the researcher intended, as well as response categories that do not capture common answers. Revising the questionnaire after testing can improve both measurement and the fieldwork process.

### SurveyCTO and field data collection

SurveyCTO allows researchers to conduct digital surveys using structured questionnaires with skip patterns, validation rules, calculations, and other controls. These features can reduce some common data entry problems and make it possible to organise field data in a consistent format.

Good digital data collection still depends on the people implementing the survey. Enumerators need appropriate training, the questionnaire needs to be piloted, and submitted interviews need to be reviewed. I am interested in using digital survey tools to prevent avoidable errors while maintaining checks for unusual or unexpected observations.

### Pilot surveys and enumerator training

A pilot survey provides an opportunity to understand how a questionnaire works under actual interview conditions. It can reveal how long interviews take, which questions are difficult to understand, whether response categories are appropriate, and where additional instructions are required.

Enumerator training is closely connected to the pilot process. Enumerators need to understand the purpose of questions while asking them consistently and without influencing respondents. Reviewing pilot interviews and discussing problems before the main survey can improve both implementation and data quality.

### Building reproducible research workflows

A reproducible research workflow should make it possible to understand how a final result was produced from the original inputs. This involves keeping raw and processed data separate, organising scripts clearly, documenting transformations, and maintaining a record of changes to code and research files.

I find this especially important when research involves repeated cleaning or several people working with the same data. A well organised workflow reduces the risk of losing files or forgetting how a result was produced. It also makes it easier to return to a project and understand the decisions that were made earlier.

### Research data and replication

Replication requires a clear path from the original data to the reported results. A researcher should be able to understand what data were used, what transformations were performed, and how the final tables or figures were generated. Clear documentation is therefore important even when the original data cannot be made publicly available.

For my own work, this means keeping track of source files, cleaning scripts, intermediate datasets, and final outputs. I also find basic checks useful before finalising an analysis, including sample sizes, missing values, summary statistics, merge results, and consistency between the underlying data and reported results.
