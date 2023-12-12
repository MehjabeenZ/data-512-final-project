# Project Part 4: Final Report

This repository contains the data files, code and results of the final project for the course Data 512: Human Centered Data Science at the University of Washington's MS in Data Science program. 

## Goal of Project
In recent years, the western United States has been experiencing increasingly severe wildfires, resulting in widespread smoke that affects multiple states. While the causes of these wildfires are debated, including factors like climate change and forestry policies, their impact is undeniable. 

This project focuses on assessing how wildfires impact Gillette, Wyoming, particularly student learning outcomes with the ultimate objective of providing valuable insights to policymakers, city administrators, and local authorities. By understanding these impacts, they can make informed decisions on how to prepare for and mitigate the consequences of future wildfires.

This project investigates two research questions: 

_What are the estimated smoke impacts on Gillette, Wyoming for the last 60 years?_

_What is the impact of air quality on student learning outcomes in Gillette, Wyoming?_

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
├── data/
│   ├── NAEP Data.xlsx
│   ├── wildfires_data.csv
├── results/
│   ├── Mehjabeen Zameer - DATA 512 Project Part 4.docx
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
- [NAEP](https://www.nationsreportcard.gov/profiles/stateprofile/overview/WY?cti=PgTab_OT&chort=1&sub=MAT&sj=WY&fs=Grade&st=MN&year=2022R3&sg=Gender%3A%20Male%20vs.%20Female&sgv=Difference&ts=Single%20Year&tss=2022R3&sfj=NP) Performance of Wyoming on the National Assessment of Educational Progress (NAEP) which is a comprehensive and nationally representative assessment that evaluates student performance in various subjects across the United States every two years.
- [Sample Notebook for Calculating Geo Distances](https://drive.google.com/file/d/1qNI6hji8CvDeBsnLDAhJXvaqf2gcg8UV/view?usp=drive_link). This code is provided under the [Creative Commons](https://creativecommons.org) [CC-BY license](https://creativecommons.org/licenses/by/4.0/). Revision 1.2 - August 14, 2023
- [Sample Notebook for Extracting Air Quality Data](https://drive.google.com/file/d/1bxl9qrb_52RocKNGfbZ5znHVqFDMkUzf/view?usp=drive_link). This code is provided under the [Creative Commons](https://creativecommons.org) [CC-BY license](https://creativecommons.org/licenses/by/4.0/). Revision 1.2 - August 14, 2023

Intermediary Files:

- [wildfires_data.csv](https://github.com/MehjabeenZ/data-512-final-project/blob/main/data/wildfires_data.csv): Wildfire incidents that occured between 1963-2023 that were less than 1250 miles from Gillette, Wyoming.  
- [NAEP data.xlsx](https://github.com/MehjabeenZ/data-512-final-project/blob/main/data/NAEP%20Data.xlsx) Educational data from the National Assessment of Educational Progress (NAEP) for the state of Wyoming. 

Some data files for the assigment were large in size (over 3 GB and 700 mb) and therefore not uploaded. However, these can be extracted using the links above and from the [code notebook](https://github.com/MehjabeenZ/data-512-project/blob/main/code/Analysis%20of%20Wildfires.ipynb). 

The table below describes the data fields in the wildfires_data.csv file:

|Column|Description|
|---|---|
|`USGS_Assigned_ID`|A unique ID assigned by the USGS creators of the dataset to the focal fire.|
|`Fire_Year`|The calendar year when the dataset creators determined the fire occurred.|
|`GIS_Acres`|The GIS calculated acres of the fire polygon calculated by using the Calculate Geometry tool in ArcGIS Pro.|
|`Distance`|Shortest distance in miles of the perimeter of the fire to Gillette.|

The table below describes the data fields in the NAEP data.xlsx file:

|Column|Description|
|---|---|
|`Subject`|Subject of the assessment – in our case, either Math or Reading.|
|`Grade`|Grade of assessment – in our case, either Grades 4 or 8.|
|`Year`|Year the assessment was conducted – from 1990 – 2022.|
|`Jurisdiction`|The jurisdiction from which data is collected – in our case, Wyoming.|
|`Average Scale Score`|Score on the assessment with scale range from 0-500. |

## Results
This study aimed to investigate the estimated smoke impacts in Gillette, Wyoming, over the last six decades and assess the potential impact of wildfire smoke on student learning outcomes. The analysis revealed an increasing trend in the number of wildfires and acres burned within 1250 miles of Gillette, aligning with broader trends reported by the US Forest Service. Correlations between AQI and math and reading test scores, while moderate to weak, were found to be negative indicating that lower air quality is associated with lower test scores. Considering the extensive body of evidence about the wide ranging impact of worsening air quality, this project recommends the city council members and residents of Gillette, Wyoming to take a proactive approach in addressing air quality concerns. 

## Special Considerations
- Step 1.6 in the notebook takes a few hours to run. In the json file, some rings are labelled as 'curverings' which may interrupt the block of code. As these records are less than 50 in a file with over 135,000 records, these have been excluded in this analysis but may be considered by anyone looking to reproduce this research. 
- The United States Environmental Protection Agency (US EPA) was created in 1973 and began installing air quality monitoring stations in the 1980s. Further, of 3000+ counties in the US, the EPA has vetted monitoring stations in only 2000 of them. Therefore, there are quite a few null values when trying to extract and use the AQI data.



