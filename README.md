# **Descriptive Analysis of License Issued in Vancouver city in 2023 and 2024 in AWS**

## **Project Overview**

The City of Vancouver is improving its services with a Data Analytics Platform (DAP), enabling smarter decision-making. My role in this project involved calculating the total number of issued and canceled licenses and identifying trends over time.

This project provides insights into number of License "issued" and Licnese that "gone out of business" in year of **2023 and 2024**, leveraging the power of AWS technologies for data storage, cleaning, analysis, and monitoring.

## **Objective**
The main goal of this project was to identify the rate of license issued and cancelled in 2023 and 2024. The analysis provided insights into cancelled and issued dental licenses to help the City of Vancouver optimize their Resource Allocation and Infrastructure Planning, Monitoring Economic Health, Compliance and Governance and Make Data-driven Decisions.

## **Dataset**
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

# **Data Analytical Question Formulation**
## **Goal**

To **analyze the rate of licnese issued or gone out of business**in years 2023 and 2024, and identify how these rates have changed over time.

## **Key Metric**

**License Issued Per year:**  This metric tracks the percentage of license issued or gone out of businesses, categorized by status, for both 2023 and 2024.

# **Methodology**

+ **1. Data Collection and Storage****
**AWS S3:** The dataset was stored in two separate S3 buckets for the years 2023 and 2024, ensuring secure and scalable storage.
+ **2. Data Cleaning and Preprocessing**
**AWS DataBrew:** The data was cleaned using AWS DataBrew to address missing values, remove duplicates, and ensure consistency across both datasets.
+ **3. ETL Pipeline**
**AWS Glue:** I used AWS Glue to build an automated ETL (Extract, Transform, Load) pipeline, which enabled efficient data extraction from S3, transformation of the data, and loading it for analysis.

![etl bsuiness license](https://github.com/user-attachments/assets/e1f245ee-c4f9-4fa0-aab1-909a397ae9ba)

 **4. Data Analysis**
 
**AWS Athena:** SQL queries were run in AWS Athena to analyze the cleaned data. I calculated the lost rate of each breed and summarized trends in lost animals across 2023 and 2024.
  
Here is the exact query used to retrieve the necessary data from Athena:

**For issued License:**

 ![QI](https://github.com/user-attachments/assets/4e8edd47-ad5b-40bd-bf29-550cf95121e2)

**For "Gone out of business" Query**

 ![QGOB](https://github.com/user-attachments/assets/5f10ff1a-4656-47b4-9d67-8bdf85e38d28)

# **Data Visualization**
**Excel:** Bar chart was created in Excel to visualize the rates of License Issued and "Gone out of Business"

**Visualization 1:** Bar chart of issued and gone out of business rates
 ![barchart dentistratae](https://github.com/user-attachments/assets/e4680fa0-185f-4929-9720-735e9bdb9f99)


# **Publishing and Web Hosting**

**AWS EC2:** The analysis and results were published on a web server using AWS EC2 to make the findings easily accessible for stakeholders.

# **Data Protection and Governance**

**AWS Key Management Service (KMS):** Encryption was applied to secure data in S3 using KMS, ensuring that data at rest and in transit was protected with cryptographic keys.

**Data Replication:** Replication rules were set to ensure data was duplicated across different AWS regions, providing redundancy in case of regional failures.

**AWS Glue:** The data was governed and managed through AWS Glue, where a tested zone was established to maintain data quality.

# **Data Monitoring**

**AWS CloudTrail:** API calls and user activities across the AWS environment were monitored using CloudTrail, enhancing auditing and security measures.

**AWS CloudWatch:** CloudWatch tracked performance metrics and resource utilization, allowing me to monitor the health of services and ensure optimal performance.

# **Data Insights and Findings**

**Rates of License Issued and Gone out of businesses** : There were less rate of business who went out of businesses in 2024 compared to 2023 

**Trends:** 2024 showed higher number of license issued than 2023

# **Recommendation:**
Based on the analysis of dental clinic license issuances and cancellations in Vancouver for 2023 and 2024, it is recommended that the city implement targeted business support programs and policy adjustments to address fluctuations in the dental sector. High cancellation rates may indicate economic challenges such as rising operational costs or regulatory burdens. To mitigate this, Vancouver could offer financial incentives like tax relief or subsidies for clinics in struggling neighborhoods, while focusing on business retention and expansion (BR&E) programs. These initiatives could include mentorship for clinic owners and infrastructure improvements in high-potential areas where new licenses are being issued. Additionally, collaboration with healthcare providers to understand industry challenges and proactive policy adjustments will foster a more supportive business environment, ensuring sustainable growth and better distribution of healthcare services across the city..

# **Tools and Technologies Used**

+ **AWS S3**: For data storage.
+ **AWS DataBrew:** For cleaning and transforming the dataset.
+ **AWS Glue:** To automate the ETL pipeline.
+ **AWS Athena:** For running SQL queries and analyzing the data.
+ **Excel:** For visualizing the data using charts and histograms.
+ **AWS EC2:** For hosting the analysis results on a web server.
+ **AWS Key Management Service (KMS):** For encryption and data protection.
+ **AWS CloudTrail:** For monitoring user activities and API calls.
+ **AWS CloudWatch:** For tracking performance metrics and monitoring system health.

# **Deliverables**
A detailed report summarizing the methods, findings, and recommendations.
Visualizations and dashboards to present key insights clearly.

# **Conclusion**
This data analytics project enables the City of Vancouver to make evidence-based decisions that benefit local businesses and residents. By understanding the trends in business licenses, the city can improve urban planning, strengthen the local economy, enhance public services, and ensure sustainable growth.
