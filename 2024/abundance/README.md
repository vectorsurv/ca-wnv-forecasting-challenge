# Data Type: Adult Female Mosquito – Abundance

This dataset includes monthly adult trapping data for Culex tarsalis, Culex pipiens complex (Culex pipiens, Culex quinquefasciatus, and their hybrids), Culex restuans, Culex stigmatosoma, Culex salinarius, and Culex nigripalpus) by county, trap type, and species.

This includes data on the total trapping effort (number of sites, trap nights, and collections) and the collections of each species (number of adults collected and number of collections in which the species was detected).

Each line represents all collections for a single county in a single month for a single trap type and species. Note that counties have multiple lines for a single month if they employed more than one trap type and/or found more than one species. If multiple species were collected for a single county, month, and trap type, the denominators for trapping effort (number of sites, trap nights, and collections) for each species remain the same and thus are repeated in each row.

## DESCRIPTION OF VARIABLES

### `state`

State of collection

Examples: Florida, California

### `statefp`

Two digit FIPS code for state of collection <https://www.census.gov/geo/reference/codes/cou.html>

Examples: 12, 06

### `county`

County of collection, without the word "County"

Examples: Broward, Los Angeles

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
- `CO2` : Traps baited with CO2, including CDC, EVS, and ABC light traps and Fay-Prince traps (BG sentinel traps using CO2 are classified separately as BGS).
- `BGS`: Biogents sentinel traps including those baited with CO2.
- `NJLT`: New Jersey light traps baited with light.
- `OTHER`: Miscellaneous other trap types targeting adult female mosquitoes that do not fall within the types listed above. This type is included for completeness to accommodate less commonly used trap types. Due to heterogeneity in the types of traps represented by this category, note that “other” trap types may be of less value for predictive modeling.

### `num_sites`

Number of distinct trap sites (i.e., geographic locations) represented within the county-month.

### `num_collection_events`

Number of distinct trap collections represented within the county-month. This may be less than the number of trap nights when traps were set for multiple nights.

### `num_trap_nights`

Cumulative number of nights distinct traps were run at all sites.

### `species`

Species of mosquitoes represented within the row. Note that species in some counties are recorded as combinations of the listed species.

### `num_adult_females_collected`

Number of collected mosquitoes identified as the indicated species.

### `num_collection_events_with_detection`

Number of collection events in which the indicated species was detected.
