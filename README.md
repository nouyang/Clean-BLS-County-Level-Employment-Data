# Clean BLS County Level Employment Data

This file cleans employment and unemployment data by County from the U.S. Bureau of Labor Statistics (BLS). These data are known as Local Area Unemployment (LAU) statistics. The raw text files are not easy to immediately manipulate, so this cleaning file produces a "long format" .csv file for ease of use.

# Getting Started

BLS LAU data are available monthly from 1990-2017, and can be found at: <https://download.bls.gov/pub/time.series/la/>. The code downloads the following raw data files from the BLS website:

- la_area.txt
- la_data_0_CurrentU90_94.txt
- la_data_0_CurrentU95_99.txt
- la_data_0_CurrentU00_04.txt
- la_data_0_CurrentU05_09.txt
- la_data_0_CurrentU10_14.txt
- la_data_0_CurrentU15_19.txt

Note that these files are each between 75mb and 131mb in size. These files can be deleted after cleaning, if the raw data is no longer needed.

# Code output

The code produces a .csv file with the following columns.

- FIPS code
- State
- County name
- Year
- Month
- Employment (level)
- Labor force (level)
- Unemployment (level)
- Unemployment rate

If all data from 1990-2017 is used, the resulting .csv file is approximately 60mb in size.

For example:
```
FIPS,state,countyname,year,month,Employment,Labor_Force,Unemployment,Unemployment_Rate
01001,AL,Autauga County,1990,1,15469.0,16519.0,1050.0,6.4
01001,AL,Autauga County,1990,2,15487.0,16581.0,1094.0,6.6
...
72153,PR,Yauco Municipio,1999,12,11578.0,13396.0,1818.0,13.6
```

# Prerequisites

The script requires 'Python' along with the 'pandas' and 'requests' libraries.

# Running the code

The code can be run directly from the command line via:
```
python BLS_LAU_County.py
```

# Author

- James Graham (NYU, 2018)

# License

This project is licensed under the MIT License.
