**Descriptive Analysis of License Issued in Vancouver city in 2023 and 2024 in AWS**

*Project Overview*

The City of Vancouver is improving its services with a Data Analytics Platform (DAP), enabling smarter decision-making. My role in this project involved calculating the total number of issued and canceled licenses and identifying trends over time.

This project provides insights into number of License issued in year of **2023 and 2024**, leveraging the power of AWS technologies for data storage, cleaning, analysis, and monitoring.

**Objective**
The main goal of this project was to identify the rate of license issued and cancelled in 2023 and 2024. The analysis provided insights into cancelled and issued dental licenses to help the City of Vancouver optimize their Resource Allocation and Infrastructure Planning, Monitoring Economic Health, Compliance and Governance and Make Data-driven Decisions.

**Dataset**
The dataset contains Number of License Issued , cancelled , goneout of business and Pending in  Vancouver, spanning December 2023 to January 2024. It includes the following key features:

+ **FOLDERYEAR:** Year of the business license folder (e.g., 2023).
+ **LicenceRSN:** Unique reference number for the license.
+ **LicenceNumber:** Official business license number.
+ **LicenceRevisionNumber:** Number of revisions to the license.
+ **BusinessName:** Registered legal name of the business.
+ **BusinessTradeName:** Trade or “doing business as” name.
+ **Status:** Current license status (e.g., Issued, Canceled).
+ **IssuedDate:** Date the license was issued.
+ **ExpiredDate:** Date the license expires.
+ **BusinessType:** General category of the business (e.g., Healthcare).
+ **BusinessSubType:** More specific business type (e.g., Dental Clinic).
+ **Unit:** Unit number of the business address.
+ **UnitType:** Type of unit (e.g., Suite).
+ **House:** Street number of the business.
+ **Street:** Street name of the business.
+ **City:** City where the business is located.
+ **Province:** Province or state (e.g., British Columbia).
+ **Country:** Country (e.g., Canada).
+ **PostalCode:** Business postal code.
+ **LocalArea:** Neighborhood or local area.
+ **NumberofEmployees:** Number of employees at the business.
+ **FeePaid:** License fee paid by the business.
+ **ExtractDate:** Date the data was extracted.
+ **Geom:** Geospatial data for mapping.
+ **geo_point_2d:** Latitude and longitude coordinates.

Dataset link: [Dental Business License Issued in 2024](https://opendata.vancouver.ca/explore/dataset/business-licences-2013-to-2024/information/?disjunctive.status&refine.issueddate=2024&refine.businesstype=Health+Services&refine.businesssubtype=Dentist)

[Dental Business License Issued in 2023](https://opendata.vancouver.ca/explore/dataset/business-licences-2013-to-2024/information/?disjunctive.status&refine.folderyear=23&refine.businesstype=Health+Services&refine.businesssubtype=Dentist)


<img width="843" alt="image" src="https://github.com/user-attachments/assets/766a6756-888e-4901-8608-fccdebb49e75">

**Data Analytical Question Formulation**
*Goal*

To analyze the rate of licnese issued or cancelled in years 2023 and 2024, and identify how these rates have changed over time.

**Key Metric**

**License Issued Per year:**  This metric tracks the percentage of license issued or cancelled, categorized by status, for both 2023 and 2024.

**Methodology**

**1. Data Collection and Storage****
**AWS S3:** The dataset was stored in two separate S3 buckets for the years 2023 and 2024, ensuring secure and scalable storage.
**2. Data Cleaning and Preprocessing**
**AWS DataBrew:** The data was cleaned using AWS DataBrew to address missing values, remove duplicates, and ensure consistency across both datasets.
**3. ETL Pipeline**
**AWS Glue:** I used AWS Glue to build an automated ETL (Extract, Transform, Load) pipeline, which enabled efficient data extraction from S3, transformation of the data, and loading it for analysis.


