# Techincal exercise

## Goal

The goal of this technical exercise is to develop a python script to automatically extract Energy and Waste Emissions Factors from a particular source (description provided below) and normalize and add them to Climatiq Emissions Factors Database (EFDB) schema. Below is a description of the source and Climatiq EFDB:

- **Source:** EPA 2023, The United States government agency that provides regularly updated default emission factors for organizational greenhouse gas reporting in the United States. **EPA_ghg-emission-factors-hub.xlsx** is the source raw data file, which is available in the Github repository shared with you.

- **Climatiq Emissions Factors Database (OpenEmissionsFactorsDB_task.csv):** A collection of up-to-date and transparent emission factors, covering carbon dioxide and all constituent gases. Data is collected from different sources and is normalized into a structured format, enriched with metadata such as validity year, CO2e calculation method, region, quality flags and LCA activity. Information on metadata is provided in **DATA_GUIDANCE.md** available in the Github repository.

## The Excersise 

Given a time constraint of 3 hours:
- Develop a python script to extract the Energy and Waste emission factors (Tables 1, 6, 9) from EPA and add them to **OpenEmissionsFactorsDB_task.csv**. For your reference, selected EPA EFs are already included in the csv file. To generate an activity_id column, use the **Sector-Category-ID_structure.csv** file as a reference. It provides a list of activity_id structures for different categories and sectors that currently exist in the EFDB. Please provide both the python script and the updated **OpenEmissionsFactorsDB_task.csv** file that contains the new data points.

- Usually after the script-based ingress, still some manual adjustments are required by the Science and Data team, for example to remove a detected anomaly, a "character" that has not been removed from the raw data. After EPA normalization and ingress in 2023, we know that in 2024, EPA will release a new dataset. How would you automate the ingress of data to not repeat any manual adjustments done?   

- Climatiq Emissions Factors Database is expanding rapidly. We collect data from a wide range of sources, each reporting in different formats (e.g. pdf, csv, xlsx) and following various schemas and update timelines. Please present an architecture design for a system that automates the ingress and updates of an increasingly large number of datasets. This design should facilitate seamless human review and collaboration.

- List out future improvements, experiments, edge cases and how they can be managed.
