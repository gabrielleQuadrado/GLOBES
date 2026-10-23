# GLOBES — Global Library of Observations from Buoys for Evaluating Sea States

GLOBES is a global archive of historical wave observations from moored buoys, designed to improve the accessibility, consistency, and reuse of in situ wave measurements across observing networks.

The first release compiles **1,665 wave buoy records from 27 data providers across 41 countries**, covering observations from **1969 to 2026**. GLOBES harmonizes wave parameters, units, timestamps, missing-value conventions, quality-control information, and station metadata while preserving original provider information and native temporal resolution.

The dataset supports research on wave climate, variability and extremes, coastal hazards, and the evaluation of numerical models, hindcasts, reanalyses, and satellite-derived wave products.

## Dataset overview

- **Platform:** Moored wave buoys
- **Spatial coverage:** Global
- **Temporal coverage:** 1969–2026
- **Data providers:** 27
- **Buoy records:** 1,665
- **Countries:** 41
- **Temporal resolution:** 10 minutes to 3 hours, depending on the source
- **Data format:** Standardized station-based text files with embedded metadata and quality-control information

## Standardized variables

Each GLOBES record contains 11 standardized columns:

| Variable | Description | Unit |
|---|---|---|
| TS (Date) | Observation date in UTC (YYYY/MM/DD) | — |
| TS (Time) | Observation time in UTC (HH:MM:SS) | — |
| HS | Significant wave height | m |
| HM | Maximum individual wave height | m |
| TP | Peak wave period | s |
| TZ | Mean wave period derived from zero-crossing analysis | s |
| TM | Mean wave period, based on the documented provider-specific estimator | s |
| DR | Representative wave direction | degrees |
| SP | Directional spread | degrees |
| FL1 | Harmonized quality-control flag | — |
| FL2 | Binary analysis-use flag | — |

Variable definitions may differ among original providers. For example, HS may represent time-domain or spectral significant wave height, while TM may correspond to different mean-period estimators. Directional conventions are retained from the original providers rather than universally converted.

The common missing-value convention is **-99.9999**.

## Quality-control flags

GLOBES includes two standardized quality-control flags derived from the information supplied by original data providers.

| FL1 | Meaning | FL2 |
|---|---|---|
| 0 | Undefined quality status | 1 |
| 1 | Good | 1 |
| 2 | Advisory (e.g., provisional or questionable) | 1 |
| 3 | Bad or rejected | 0 |
| 9 | Missing | 0 |

**FL2 = 1** indicates observations retained for analysis under the GLOBES harmonized flagging conventions, while **FL2 = 0** indicates observations excluded from analysis.

These flags do not represent an independent quality-control assessment performed by GLOBES. Companion quality-control files preserve additional provider-specific information where available.

## Metadata and file structure

Each main data file contains a metadata header followed by observations organized by UTC timestamp.

Metadata include station identifiers, geographic coordinates, temporal coverage, contributing and originating organizations, record characteristics, variable definitions, quality-control information, and applicable data-use conditions.

Individual files are identified using station names, station codes, country codes, and provider acronyms. Separate records associated with the same nominal station may be distinguished by alphabetical suffixes.

## Data access and versions

GLOBES will be archived through Zenodo in versioned releases. Each version will provide a reproducible snapshot of the available dataset.

**Dataset DOI:** To be added after the first Zenodo publication.

This repository provides an overview of the dataset, standardized variables, file conventions, and conditions of use.

**Release status:** Preliminary. Data files and associated metadata remain subject to updates and refinements before the first stable release.

## Data use and attribution

GLOBES integrates observations from multiple organizations with different licensing and usage conditions. Original data ownership remains with the contributing providers or originators.

Applicable conditions are specified in the **USAGE** metadata field of individual buoy records. These may permit unrestricted use, limit use to non-commercial or academic purposes, or require additional authorization.

Users must comply with the applicable provider-specific conditions and attribution requirements. Inclusion in GLOBES does not replace the original provider's license or grant additional redistribution rights.

## Citation

Please cite the GLOBES dataset when using its standardized observations in scientific publications, analyses, or derived products.

Quadrado, G. P., Haigh, I. D., Nagaraj, M., Hague, B. S., Carneiro-Barros, J. E., and Wahl, T.: *GLOBES: the Global Library of Observations from Buoys for Evaluating Sea States*, Zenodo, [version], [DOI], [year].

The final citation will be updated following publication of the first Zenodo release.

## Contact

Gabrielle P. Quadrado  
University of Central Florida  
gquadrado@ucf.edu
