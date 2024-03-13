# Techincal exercise

## Goal

The goal of this technical exercise is to develop a python script to automatically extract Energy and Waste Emissions Factors from a particular source (description provided below) and normalize them to Climatiq Emissions Facors Database (EFDB) schema and add them to the EFDB. Below is a description of the source and Climatiq EFDB:

- **Source:** EPA 2023- The United States government agency that provides regularly updated default emission factors for organisational greenhouse gas reporting in the United States. EPA_ghg-emission-factors-hub.xlsx is the source raw data file, which is available in the Github repository shared with the candidate.
- **Climatiq Emissions Factors Database (OpenEmissionsFactorsDB_task.csv):** A collection of up-to-date and transparent emission factors, covering carbon dioxide and all constituent gases. Data is collected from 30+ sources and is ingestible in a structured format, enriched with metadata such as validity year, source, CO2e calculation method, region, quality flags and LCA activity. Information on metadata is provided in DATA_GUIDANCE.md available in the Github repository. 

## The Excersise 

Given a time constraint of 3 hours:
- Develop a python script to extract the Energy and Waste emission factors (Tables 1, 2, 6, 9) from EPA and add them to OpenEmissionsFactorsDB_task.csv. For your reference, selected EPA EFs are already included in the csv file. To generate activity_id column, use the Sector-Category-ID_structure.csv file as a reference. It provides a list of activity_id structures for different categories and sectors that currently exist in the EFDB.
- Usually after the script-based ingress, still some manual adjustments is required by the data team for example to remove a detected anomaly, a "character" that has not been removed from the raw data. Or some manual adjustments might be needed for the activity_id structurs with more than 1 sub ID e.g.  fuel-type[..]-fuel_use[....].  After EPA normalization and ingress in 2023, we know that in 2024, EPA will release a new dataset. How would you automate the ingress of data to not repeat any manual adjustments done? Please present an architecture design for a system that incorporates automation of ingress and updates along with human reviews and collaboration.   
- List out future improvements, experiments, edge cases and how they can be managed.
