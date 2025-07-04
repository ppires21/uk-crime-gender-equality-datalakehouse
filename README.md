# UK Crime and Gender Equality Data Lakehouse

This repository contains the final project for the "Data Engineering for Decision Support" course (2023/2024) at University of Minho, focused on the analysis of crime in the United Kingdom in the context of gender equality. 

## Table of Contents
- [Project Overview](#project-overview)
- [Datasets](#datasets)
- [Technologies Used](#technologies-used)
- [Architecture](#architecture)
- [Analytical Questions & KPIs](#analytical-questions--kpis)
- [Dashboards](#dashboards)
- [Team](#team)

---

## Project Overview

The aim of this project is to conduct an in-depth descriptive analysis of crime in the UK with a special focus on gender equality. Using a Data Lakehouse architecture, we integrated and processed several public datasets related to homicides, police stop-and-search operations, gender statistics, and child protection in London.

The project covers:
- Data quality assessment and profiling
- ETL processes (Bronze, Silver, Gold layers)
- Dimensional modelling (Star Schemas)
- Analytical dashboards in Tableau
- Insights on the relationship between gender and crime patterns, victimisation, policing, and child protection

---

## Datasets

- **Homicide (London, 2003-2023):** Victims and offenders by borough, method, age, gender, outcome
- **Stop-and-Search (UK):** Police stop/search operations by gender, legislation, object, location, age group, officer ethnicity (2017-2023)
- **Gender Statistics:** World gender indicators (focused on UK) such as mortality rates, population by age/gender, etc.
- **Children Care Plan:** Child protection cases in a London borough, including abuse categories, plan duration, demographics

Most datasets were obtained from [data.london.gov.uk](https://data.london.gov.uk/), [data.police.uk](https://data.police.uk/), and resources provided by the course lecturers.

---

## Technologies Used

- **Talend Open Studio:** Data profiling & quality assessment
- **Apache Spark & Hive (HDFS):** Data Lakehouse ETL pipelines (Bronze, Silver, Gold layers)
- **JupyterLab:** Data exploration & scripting
- **Tableau Desktop:** Dashboarding & data visualisation
- **Trino & Presto:** Analytical querying

---

## Architecture

The solution adopts a classic Data Lakehouse layered architecture:

- **Bronze Layer:** Raw data ingestion and storage in HDFS
- **Silver Layer:** Cleaned, transformed, and integrated data tables
- **Gold Layer:** Star schema fact/dimension tables for analytics

![](docs/architecture.png) <!-- Insert your diagram here -->

Each dataset was processed through standard ETL steps, with artificial keys added for dimensional modelling, standardisation of age groups/gender fields, and cleaning of location data to enable consistent analysis across sources.

---

## Analytical Questions & KPIs

**Example analytical questions addressed:**
- What are the age/gender discrepancies in UK population from 2010-2022?
- How do infant mortality and intentional homicides differ by gender?
- What are the trends and gender differences in stop-and-search operations?
- Are the boroughs with the most male homicide victims the same as for females?
- Which age/gender groups are most affected as homicide victims and offenders?
- Are there significant gender differences in child protection plans?

**Sample KPIs:**
- Total number and percentage of homicides, offenders, stop-and-search cases by gender
- Ratio between male and female victims/offenders
- Mean duration of child protection plans by gender
- Most common homicide methods by gender over time

For more details, see the [report](PL3_G3_EntregaFinal.pdf).

---

## Dashboards

The final analysis is presented via interactive dashboards in Tableau, allowing for dynamic filtering by gender, age, location, time, outcome, and other dimensions.

Key dashboards include:
- Gender Data per Country (UK focus)
- Stop and Search in UK
- Homicide Victims in London
- Homicide Offenders in London
- Children Care Plan (Barnet)

Screenshots and dashboard explanations are provided in the `/docs` folder.

---

## Team

- Catarina Brandão Fernandes (a101441) - [a101441@alunos.uminho.pt](mailto:a101441@alunos.uminho.pt)
- Maria Inês da Costa Maia (a93347) - [a93347@alunos.uminho.pt](mailto:a93347@alunos.uminho.pt)
- Pedro Miguel Araújo Pires (a95549) - [a95549@alunos.uminho.pt](mailto:a95549@alunos.uminho.pt)
- Liandro Macedo da Cruz (a100436) - [a100436@alunos.uminho.pt](mailto:a100436@alunos.uminho.pt)

---

## License

For academic purposes only.

---

> This project was developed for the "Data Engineering for Decision Support" course (2023/2024) at University of Minho.
