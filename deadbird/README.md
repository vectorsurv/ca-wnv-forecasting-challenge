# Data Type: Dead Bird

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

### `num_positive_deadbirds`

Number of birds that tested positive in the specified county in that month
