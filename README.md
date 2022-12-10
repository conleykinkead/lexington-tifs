# TIF-Funded Developments in Lexington, KY

## Data sources used
- [TIF District](https://data-lfucg.hub.arcgis.com/datasets/3a457d1e28464d9dbcbe3091c0b810d6_0/about) from Lexington Fayette Urban County Government (LFUCG). Polygons of the eight properties in Lexington, KY approved for Tax Increment Financing (TIF) funding. TIF funding began in Lexington in 2009.
- Census tract boundaries from [TIGER/Line](https://www.census.gov/cgi-bin/geo/shapefiles/index.php).
- Median household income, 2010, from American Community Survey, [US Census Bureau](https://data.census.gov/).
- Median household income, 2019, from American Community Survey, [US Census Bureau](https://data.census.gov/).

## Description of the map's creation and purpose
I'm interested in studying gentrification and displacement in Lexington. Since 2009, Lexington has supported 8 developments through Tax Increment Financing (TIF), a lending strategy that the city turned to to encourage redevelopment of sites that were depressing surrounding property values (Ward and Wood, 2021). This maps shows Lexington's 8 TIF developments and the change in median household income (MHI) of all census tracts in Lexington from 2010-2019. A change in MHI in census tract may indicate that the population has shifted to consist of higher- or lower-income individuals--signifying gentrification or disinvestment, respectively. Census tracts that are orange had an decrease in MHI from 2010-2019; census tracts that are purple had a increase in MHI from 2010-2019.

TIF funding is controversial because it is a way of subsidizing private development projects with public dollars, usually going to politically connected developers. Addionally, if the district is successfully revitalized, it often causes gentrification in surrounding areas.

To make this map, I cleaned the median household income (MHI) tables using R and Excel to remove margin of error columns and calculate MHI in 2022 dollars. I then moved to QGIS to join MHI tables to the census tract boundaries, and deducted 2010 MHIs from 2019 MHIs for each census tract using the field calculator. The change in the MHI is reflected by the census tract colors: orange indicates a decrease in MHI, and purple indicates an increase in MHI. The TIF District polygons are layered on top so the viewer can see the change in census tract MHI relative to the projects.

Income data from 2010 and 2019 were adjusted to 2022 dollars based on results from the [CPI Inflation Calculator](https://www.bls.gov/data/inflation_calculator.htm) from the US Bureau of Labor Statistics. $1.00 in 2010 had the same buying power as $1.36 in 2022; $1.00 in 2019 had the same buying power in as $1.16 in 2022.
