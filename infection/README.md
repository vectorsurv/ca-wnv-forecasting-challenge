# Data Type: Adult Female Mosquitoes – West Nile virus infection

This dataset includes monthly testing of adult female mosquitoes for West Nile virus by county and trap type. Mosquitoes are commonly tested in pools (i.e., batches) of 1-50 mosquitoes per pool. These data include information on the total testing volume (number of pools tested, and number of mosquitoes tested) and the results of testing for West Nile virus (number of pools positive for West Nile virus).

Each line represents all collections for a single county in a single month for a single trap type and species. Note that counties have multiple lines for a single month if they employed more than one trap type and/or tested more than one species.

## DESCRIPTION OF VARIABLES

### `state`

State of collection

Examples: Florida, California

### `statefp`

Two digit FIPS code for state of collection <https://www.census.gov/geo/reference/codes/cou.html>

Examples: 12, 06

### `county`

County of collection, without the word "County"

Examples: Monmouth, Los Angeles

### `countyfp`

Three digit FIPS code for county of collection <https://www.census.gov/geo/reference/codes/cou.html>

Examples: 011, 037

### `year`

Four digit year of collection

Examples: 2016, 2017

### `month`

Numeric month of collection (1-12)

Examples: 1, 10

### `trap_type`

Type of trap used for collection, includes:

- `GRAV`: Traps that target gravid females with open water containers, including CDC and Reiter-Cummings style gravid traps.
- `CO2`: Traps baited with CO2, including CDC, EVS, and ABC light traps and Fay-Prince traps (BG sentinel traps using CO2 are classified separately as BGS).
- `BGS`: Biogents sentinel traps including those baited with CO2.
- `OTHER`: Miscellaneous other trap types targeting adult female mosquitoes that do not fall within the types listed above. This type is included for completeness to accommodate less commonly used trap types. Due to heterogeneity in the types of traps represented by this category, note that “other” trap types may be of less value for predictive modeling.

Note: NJ light traps are typically used only for abundance because mosquitoes are killed after entering the trap, and traps are left out for extended periods. Therefore, they appear as a unique trap type in the mosquito abundance file but not in the WNV infection data because mosquitoes from NJ light traps are not commonly tested for WNV.

### `species`

Species of mosquitoes represented within the row. Note that species in some counties are recorded as combinations of the listed species.

### `num_pools`

Number of mosquito pools of the indicated species tested for WNV within the county-month.

### `num_mosquitoes`

Number of mosquitoes of the indicated species tested for WNV within the county-month.

### `num_pools_wnv`

Number of pools of the indicated species found to be infected with WNV within the county-month. Nearly all testing is performed by RT-PCR, although rarely other testing methods (e.g., RAMP or VecTest) have been performed in a small number of counties.
