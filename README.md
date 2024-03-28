# California WNV Forecasting Challenge**

**DRAFT**

This is the data repository for the 2024 CDPH West Nile virus Forecasting Challenge. This is an open (_by request_) forecasting challenge to predict monthly West Nile virus (WNV) total disease cases in select California counties in 2024 in the months of May through October. This is the first iteration of a California county-specific Forecasting Challenge.

### **Forecast Reports**

If sufficient forecasts are available, forecast summary reports will be released monthly when possible through the challenge and will be available in this repository. These reports aggregate submissions from modeling teams, a forecast ensemble developed from individual model submissions, 10-year historical medians, and other baseline models. All forecasts are provided at the county-month level through the end of the year and predict total reported cases of West Nile virus disease.

### **Participation**

To participate in the Challenge, please follow these steps:

1. Contact [modeling@cdph.ca.gov](mailto:modeling@cdph.ca.gov) for instructions on how to request data and participate in the challenge.
2. Prepare metadata for your model.
3. Submit forecasts by the deadlines.

For information on submitting forecasts to this project, please see the [submission instructions](https://github.com/cdcepi/WNV-forecast-project-2023/blob/main/Forecast-Submission.md). Participating teams provide their forecasts in a multi[bin-based format](https://github.com/cdcepi/WNV-forecast-project-2023/blob/main/Forecast-Submission.md#Data-formatting) that will be evaluated according to [these criteria](https://github.com/cdcepi/WNV-forecast-project-2023/blob/main/Evaluation.md).

### **Timeline**

- Project announcement and historical data release: March 25, 2024.
- Initial forecast submission due: April 30, 2024.
- Subsequent forecast submissions due at the end of each month through September: May 31, June 30, July 31, August 31, and September 30, 2024.
- Each forecast submission should include forecasts for all remaining months of 2024 (through October).

### **Available and Suggested Data Resources**

- Human WNV case data: county-month WNV case counts reported to the CDPH are available through request as detailed.
- Mosquito data: recent and historical county-month mosquito abundance and infection data is available through our partners at VectorSurv and local public health agencies.
- Environmental data: a list of optional resources for climate and other [environmental data](https://github.com/cdcepi/WNV-forecast-project-2023/blob/main/Data-Environmental.md) are provided. If you come across other resources, please let us know and we'll add them to the list.

## **Background**

[West Nile virus](https://westnile.ca.gov/) (WNV) is the leading cause of vector-borne disease in California and the leading cause of arboviral disease in the continental United States. An estimated 80% of WNV infections are asymptomatic; ~20% of infected persons develop febrile illness and <1% of infected persons develop neuroinvasive disease (e.g., meningitis, encephalitis, or acute flaccid paralysis). Among patients with neuroinvasive disease, the case-fatality ratio is approximately 10%. Because of its severity and distinctive clinical features, diagnosis and reporting of neuroinvasive disease is considered more consistent and complete than that of non-neuroinvasive disease.

The first cases of WNV disease in the United States were identified in New York City in 1999; the virus subsequently spread westward, reaching southern California in 2003. Since then, WNV has been transmitted every year in California, particularly in the Central Valley and southern California, with intermittent years reaching epidemic levels. No vaccine or specific treatment of WNV is currently available. The only form of prevention is reducing mosquito exposure through vector control and personal protective behaviors. Predicting where and when WNV transmission will occur could help direct control efforts.

Previous national WNV forecasting challenges were run in [2020,](https://github.com/cdcepi/WNV-forecast-project-2020) [2022,](https://github.com/cdcepi/WNV-forecast-data-2022) and [2023.](https://github.com/cdcepi/WNV-forecast-project-2023/) The 2020 and 2022 challenges focused on predicting total WNV neuroinvasive disease cases in US counties over those two calendar years. [Results from the 2020 challenge](https://parasitesandvectors.biomedcentral.com/articles/10.1186/s13071-022-05630-y) showed that models based on historical case data outperformed more sophisticated models. The 2023 challenge focused on state-level outcomes (rather than county-level outcomes) to assess the ability of forecasts to predict larger scale differences between years. Moreover, the 2023 challenge focused on monthly rather than yearly outcomes, so that models can be assessed for their ability to predict when cases will occur, not just how many are reported, and will have the opportunity to integrate real-time data within the season.

The 2024 California WNV forecasting challenge draws significant inspiration from these national forecasting challenges and is now targeting **county-month** outcomes for high burden counties in order to improve public health and vector control agencies’ resource distribution in California.

**Data License and Reuse**

We are grateful to the teams who have generated forecasts and made their forecast data publicly available under different terms and licenses. By default, forecasts are available under the CC-BY 4.0 license, although teams may specify release under a different license in their metadata. You will find the licenses (when provided) within the metadata contained within model-specific folders in the data-forecasts directory. Please consult these licenses before using these data to ensure that you follow the terms under which these data were released.

## **Forecast Submission Instructions**

County-level forecasts for total WNV diseases cases in each remaining calendar month of 2024 through October should be produced and submitted by their respective monthly due dates, beginning on April 30, 2024. Please note that these monthly county-level forecasts differ from previous national WNV forecasting challenge targets. This page includes information on how to submit forecasts. These instructions have been adapted from the prior challenges and the most up to date [hubverse structure](https://hubdocs.readthedocs.io/en/latest/).

All forecasts should be submitted directly to the _model-output_ folder in this repository (more information on folder's structures is available [here](https://hubdocs.readthedocs.io/en/latest/user-guide/model-output.html)). Forecast data should be added to the repository through a pull request so that automatic data validation checks are run.

These instructions provide detail about the data format as well as validation that you can do prior to this pull request. In addition, we describe the metadata that each model should provide.

## **Data Formatting**

The automatic checks in place for forecast files submitted to this repository validate both the filename and file contents to ensure the file can be used in the visualization and ensemble forecasting.

### Subdirectory

Each subdirectory within the _model-output_ directory should have the format

team-model

where

- team is the name of your team and
- model is the name of your model.

Both team and model should be less than 15 characters and not include hyphens or other special characters (with the exception of "\\\_"). The model should be unique from any other model in the project.

Within each team subdirectory a set of forecasts should be submitted in CSV format. The name of these files should follow this convention:

- _round-id1_.csv
- _round-id2_.csv
- ...

where the _round_ corresponds to the target date of the forecast and the _id1_ to the _team-model_ identifier. More information on these folders structures is found in [this document](https://hubdocs.readthedocs.io/en/stable/format/model-output.html)

### Metadata

A metadata file should be provided by each team. This file should be placed in the _model-metadata_ folder of the repository, and should have the following [naming convention](https://hubdocs.readthedocs.io/en/stable/format/model-metadata.html):

team-model.yml

Its contents should adhere to [hubverse’s standards.](https://hubdocs.readthedocs.io/en/stable/format/model-metadata.html) Where the fields required in our challenge are: _schema_version_, _team_name, team_abbr_, _model_name_, _model_abbr_, _model_contributors_, _license_, _model_details._

### License (optional)

By default, forecasts are released under a [CC-BY 4.0 license](https://creativecommons.org/licenses/by/4.0/legalcode.en). If you would like to release your forecasts under a different license, please specify a standard license in the license field of your metadata file. Alternatively, if you wish to use a license that is not in the list of [standard licenses](https://hubdocs.readthedocs.io/en/stable/format/model-metadata.html?highlight=license#template-metadata-schema-file), you may include a

LICENSE_NAME.txt

file in the metadata folder, and refer to it in the license field of your model’s yaml file.

**Forecasts**

Each forecast file should have the following format: _YYYY-MM-DD-team-model.csv_; where

- _YYYY_: is the 4 digit year,
- _MM_: is the 2 digit month,
- _DD_: is the 2 digit day,
- _team_: is the team name, and
- _model_: is the name of your model.

The date YYYY-MM-DD is the _reference_date_. This should be at most one of the challenges deadline dates. The _team_ and _model_ in this file must match the ones in the directory this file is in. Both _team_ and _model_ should be less than 15 characters, alpha-numeric and underscores only, with no spaces or hyphens.

**Forecast file format**

The file must be a comma-separated value (csv) file with the following columns (in any order):

- _model_id_
- _location_
- _reference_date_
- _target_date_
- _bin_start_
- _bin_end_
- _value_
- _type_
- _unit_
- _model_version_

No additional columns are allowed.

**model_id**

String identifier in the form _INSTITUTION-MODEL_ (should match the one in the filename).

**location**

Values in the _location_ column must be one of the California counties in the following list: Fresno, Kern, Los Angeles, Merced, Orange, Placer, Riverside, Sacramento, San Bernardino, San Joaquin, Solano, Stanislaus, Tulare.

**origin_date**

Values in the _origin_date_ column must be a date in the ISO format _YYYY-MM-DD._ This is the date from which all forecasts should be considered. This date must be equal or lower to the submission date for each of the challenge's deadlines.

**target_date**

Values in the _target_date_ column must be a date in the format _YYYY-MM-DD._ This is the last date of the forecast target for each month. This date should match the submission target date.

**bin_start**

Lower, non-inclusive, bound on the standardized bin interval. The defined intervals for the challenge follow:

- _(0, 0\] point_
- _(0, 1\] bin_
- _(1, 2\] bin_
- _(2, 3\] bin_
- _(3, 4\] bin_
- _(4, 5\] bin_
- _(5, 6\] bin_
- _(6, 8\] bin_
- _( 8, 10\] bin_
- _(10, 15\] bin_
- _(15, 200\] bin_

where the units in each interval are in reported WNV cases per million persons per month.

**bin_end**

Upper, inclusive, bound on the standardized bin interval. Allowed interval values are defined in the **_bin_start_** section.

**type**

Either _point_ for the 0 cases prediction, or _bin_ for any other interval as described in the _bin_id_ section of this document.

**value**

Fractional quantities in the _value_ column are non-negative numbers indicating the probability assigned to the number of cases per million inhabitants falling within the given interval. The sum of the probability values for the collection of intervals in each location should total 1 (to floating point precision) for a submission to be considered valid.

**unit**

String constant with value _WNV cases_, as it is the standard unit for this challenge.

**model_version**

String URL constant containing the github's release (if available). For a guide on how to manage these releases follow [this guide](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository).

## **Forecast Validation**

To ensure proper data formatting, automatic validations are run on all pull requests to model-outputs/.

### **Pull Request Forecast Validation**

When a pull request is submitted, the data are validated through [GitHub Actions](https://docs.github.com/en/actions) which runs the tests present in [the validations folder of the repository](https://github.com/Chipdelmal/WNVCA-2024/tree/main/hub-validation). The intent for these tests are to validate the requirements above. Please [let us know](https://github.com/Chipdelmal/WNVCA-2024) if you are facing issues while running the tests.

## **Late or Updated Submissions**

To ensure that forecasting is done in real-time, all forecasts are required to be submitted to this repository by the listed deadlines. Late forecasts may be accepted on a case-by-case basis.

### **Evaluation**

When reported data for 2024 are available, an analysis will be conducted using multiple scoring metrics, including the logarithmic score and the multibin logarithmic score, to assess and compare forecasts across all counties at each time point. A joint manuscript will be prepared to disseminate findings on this comparison and the general performance of submitted forecasts. Participants may publish their own forecasts and results at any time.

**References**

- Gneiting T and AE Raftery. (2007) Strictly proper scoring rules, prediction, and estimation. Journal of the American Statistical Association. 102(477):359-378. Available at: <https://www.stat.washington.edu/raftery/Research/PDF/Gneiting2007jasa.pdf>.
- Reich NG, et al. (2019) A collaborative multiyear, multimodel assessment of seasonal influenza forecasting in the United States. PNAS. Available at: <https://doi.org/10.1073/pnas.1812594116>
