# Mosquito Data

Participants may use [mosquito abundance and infection data](https://github.com/vectorsurv/ca-wnv-forecasting-challenge) compiled by [VectorSurv](https://vectorsurv.org/) to supplement their forecast models. Initial data files will be available on the next day following March 31, 2024, including all available historical data from 2003 through the release date. Updated data will be released immediately following the 15th of each month beginning in April. 

## Notes:

- The data available for mosquito surveillance represent a subset of all counties within the continental U.S. Data are provided through partnerships with local vector control and public health agencies using VectorSurv (see list below) and represent all data in the VectorSurv system for participating agencies at the time of each data release. 
- The agencies represented in these data have opted to provide their surveillance data to inform model predictions. 
- Differences in the time periods of available mosquito data exist between agencies (e.g., time period of available historical data, trap types, and species represented) and not all states collect mosquito data. Some agencies who have elected to contribute data for this year's forecasting challenge may not have historical data in VectorSurv prior to 2023.
- Data are organized into folders by creation date.  The initial data set includes all data in VectorSurv for participating agencies as of 2023-03-31, and new datasets will include all cumulative data through the 15th of every month thereafter. Once each data set is posted, that data set will not change.
- Because these data are managed by many individuals and surveillance programs throughout the country, they cannot be validated prior to distribution. Vector control and public health partners regularly review the data and utilize them to guide their decisions, but please note that errors are possible, and the data are provided as-is without any guarantee of their accuracy or utility for forecasting or other purposes. 
- Historical data may differ between posted versions of the data set (e.g., due to edits to past data or additions of historical data that were not previously in VectorSurv). It is also possible that a small number of additional VectorSurv partner agencies will elect to contribute data after the initial release, which could result in more counties represented in subsequent releases. For these reasons, each posted data set will be a complete copy of **all** data available from 2003 through each release date.

### [Mosquito Abundance Data](https://github.com/vectorsurv/ca-wnv-forecasting-challenge/abundance)
This dataset includes monthly adult trapping data for *Culex tarsalis*, *Culex pipiens* complex (*Culex pipiens*, *Culex quinquefasciatus*, and their hybrids), *Culex restuans*, *Culex stigmatosoma*, *Culex salinarius*, and *Culex nigripalpus*) by county, trap type, and species. This includes data on the total trapping effort (number of sites, trap nights, and collections) and the collections of each species (number of adults collected and number of collections in which the species was detected).

### [Mosquito Infection Data](https://github.com/vectorsurv/ca-wnv-forecasting-challenge/infection)
This dataset includes monthly testing of adult female mosquitoes for West Nile virus by county and trap type. Mosquitoes are commonly tested in pools (i.e., batches) of 1-50 mosquitoes per pool. These data include information on the total testing volume (number of pools tested and number of mosquitoes tested) and the results of testing for West Nile virus (number of pools positive for West Nile virus). Some counties may report mosquito infection data without corresponding mosquito abundance data. For such areas, modelers should be aware that the total number of mosquitoes tested for West Nile virus is not a reliable proxy for mosquito abundance.

Detailed descriptions of each dataset are provided in data dictionaries within the individual directories for data on vector abundance and infection.

## Citations and Acknowledgements

Please cite VectorSurv in any publications that utilize these mosquito surveillance data, which helps us to justify VectorSurv's data services. A suggested citation is below:

VectorSurv Development Team. 2023. VectorSurv: Vectorborne Disease Surveillance System. URL: [https://vectorsurv.org](https://vectorsurv.org)

These data are generated by the hard work of our many partner agencies listed below who have chosen to provide their surveillance data in an open-access format for your use. Please acknowledge their contributions wherever possible (e.g., by listing the agencies in acknowledgements or a supplementary table in publications).

### California
- Alameda County Mosquito Abatement District
- Alameda County Vector Control Services District
- Butte County Mosquito and Vector Control District
- Coachella Valley Mosquito and Vector Control District
- Colusa Mosquito Abatement District
- Consolidated Mosquito Abatement District
- Contra Costa Mosquito and Vector Control District
- Delta Mosquito and Vector Control District
- East Side Mosquito Abatement District
- Fresno Westside Mosquito Abatement District
- Glenn County Mosquito and Vector Control District
- Greater Los Angeles County Vector Control District
- Kern Mosquito & Vector Control District
- Marin/Sonoma Mosquito and Vector Control District
- Mosquito and Vector Management District of Santa Barbara County
- Placer Mosquito and Vector Control District
- Presidio Trust
- Riverside County Environmental Health-Vector Control
- Sacramento-Yolo Mosquito and Vector Control District
- San Gabriel Valley Mosquito and Vector Control District
- Santa Clara County Vector Control District
- Shasta Mosquito and Vector Control District
- Sutter-Yuba Mosquito & Vector Control District
- Turlock Mosquito Abatement District
- Ventura County Vector Control Program
- West Valley Mosquito & Vector Control District
