# Project Part 4: Final Report

This repository contains the data files, code and results of the final project for the course Data 512: Human Centered Data Science at the University of Washington's MS in Data Science program. 

## Goal of Project
In recent years, the western United States has been experiencing increasingly severe wildfires, resulting in widespread smoke that affects multiple states. While the causes of these wildfires are debated, including factors like climate change and forestry policies, their impact is undeniable. 

This project focuses on assessing how wildfires impact Gillette, Wyoming, with the ultimate objective of providing valuable insights to policymakers, city administrators, and local authorities. By understanding these impacts, they can make informed decisions on how to prepare for and mitigate the consequences of future wildfires.

(Add about the education extension here)

## Goal of Assignment

The goal of this assignment is to answer the following research question: 

_What are the estimated smoke impacts on Gillette, Wyoming for the last 60 years?_

This assignment creates an estimate of wildfire smoke. This estimate is a number that will eventually be used to build a predictive model. Technically, smoke impact should probably be considered the health, tourism, economic or other social problems that result from the smoke. The smoke estimates adheres to the following conditions:

* The estimate only considers the last 60 years of wildland fires (1963-2023).
* The estimate only considers fires that are within 1250 miles of your assigned city.
* An annual fire season will run from May 1st through October 31st.

(Add about the extension research question)

## Resources Used
- Editor used: VS Code
- Python version: 3.9.18
- Packages used: json, time, pyproj, geojson, tqdm, pandas, requests, datetime, collections, seaborn, 
matplotlib, numpy, statsmodels.

## API Documentation
- [Pyproj](https://pyproj4.github.io/pyproj/stable/index.html)
- [geojson](https://pypi.org/project/geojson/)
- [Air Quality System API](https://aqs.epa.gov/aqsweb/documents/data_api.html)

## Project Organization

This project has the following structure:
```
.
├── results/
│   ├── Mehjabeen Zameer - Final Report
├── code/
│   ├── Analysis of Wildfires.ipynb
├── LICENSE
└── README.md
```

## Steps to Reproduce This Research

1. Install the required resources as listed in the Resources header above. 
2. Run the Analysis of Wildfires.ipynb file. A valid email address will be required for one step. 
3. Analyze and review results. 

## Data 

Source Files:
- [Wildfire dataset](https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81) This dataset was collected and aggregated by the US Geological Survey.  
- [FIPS](https://www.census.gov/library/reference/code-lists/ansi.html) The Federal Information Processing Standard Publication (FIPS) is a five-digit Federal Information Processing Standards code which uniquely identified counties and county equivalents in the United States, certain U.S. possessions, and certain freely associated states.
- [Sample Notebook for Calculating Geo Distances](https://drive.google.com/file/d/1qNI6hji8CvDeBsnLDAhJXvaqf2gcg8UV/view?usp=drive_link). This code is provided under the [Creative Commons](https://creativecommons.org) [CC-BY license](https://creativecommons.org/licenses/by/4.0/). Revision 1.2 - August 14, 2023
- [Sample Notebook for Extracting Air Quality Data](https://drive.google.com/file/d/1bxl9qrb_52RocKNGfbZ5znHVqFDMkUzf/view?usp=drive_link). This code is provided under the [Creative Commons](https://creativecommons.org) [CC-BY license](https://creativecommons.org/licenses/by/4.0/). Revision 1.2 - August 14, 2023

(Add NAEP data too)





