
# **UK Job Market & Visa Sponsorship Analyzer**

The UK job market is highly competitive for international candidates, especially those requiring visa sponsorship. 

This project analyzes different job listings to identify:
- Which domains have higher visa sponsorship opportunities.
- Companies that offer visa sponsorship.
- Top job platforms offering sponsored jobs.
- Top locations in the United Kingdom that offer visa sponsorship.


## **Tools & Technologies**
- Python
   - Web scraping using **SerpAPI**
   - **Data transformation:** converting raw data into structured format
   - Converting JSON data into Excel format using **Pandas**

- Microsoft Excel
  - Data cleaning and analysis using **Power Query Editor**
  - Data manipulation using **Excel formulas**
  - **Pivot Tables** for summarization
  - **Charts** and **dynamic dashboard** creation
## **Data Collection**

Job data was collected using an **automated Python script** that retrieves job listings from Google Jobs through SerpAPI. The script **searches for multiple job roles in the United Kingdom** and gathers data across several pages to ensure wider coverage.

To improve efficiency, it avoids collecting duplicate data and saves the results in structured files for further analysis. Multiple searches are processed simultaneously to speed up the data collection process.

```
Source Code : https://github.com/jagroop-dev-11/jobs_scrapper
```
## **Data Cleaning & Preparation**
- Cleaned dataset by removing duplicate job listings (112 duplicates removed, final size: 758 rows)
- Converted long job IDs into simplified numeric format for better readability.
- Created a new **Visa Sponsorship column** by identifying keywords in job titles.

- Standardized location data:
    - Extracted place names from “place, UK” format. 
    ```
    For example:
    Aberdeen, United Kingdom -> Aberdeen
    ```
    - Replaced missing provinces with “United Kingdom”
    - Removed Qualifications column due to insufficient and inconsistent data
    ```
    Qualification column have 2 values : 
      -  Null
      -  No degree mentioned
    ```

- Processed salary data:
   - Separated salary amount and salary period (monthly, weekly,  yearly, hourly etc. as mentioned in the salary details)
   - Split salary range into minimum and maximum salary

- Extracted job domain/category from job titles
## **Exploratory Data Analysis (EDA)**
<img width="972" height="586" alt="image" src="https://github.com/user-attachments/assets/b241336d-32aa-49a1-b131-ced914f3c07e" />


### Visa Sponsorship by Companies  
- Analyzed companies offering visa sponsorship along with their job posting frequency  

- **Top contributors**:  
  - Career.zycto: 11 listings **(highest contributor)**  
  - Hiring.zycto: 7 listings  
  - Career.aliyucares: 6 listings  
  - Destinydot: 3 listings  
  - NewsNowGh: 2 listings  

- **Companies with minimal presence (1 listing each):**
  - USI Global Recruitment  
  - USI Global Academy  
  - Malmin Dental Care  
  - China Link ESL  
  - RGH Global  
  - Hope Park House  
  - Vets For Pets  
  - Medmatch  
  - Collins Aerospace  
  - The Curare Group  
  - Myton Green Children's Nursery and Preschool  

- **Insight:**  
  - Visa sponsorship opportunities are **highly concentrated in a few platforms/aggregators (zycto, aliyucares)** rather than traditional employers.  
  - Most companies contribute **only a single listing**, indicating fragmented and limited sponsorship availability.  
  - The presence of healthcare, education, and recruitment firms suggests **sector-specific demand**.

---

### Sponsorship Demand by Job Domain  
<img width="976" height="591" alt="image" src="https://github.com/user-attachments/assets/3e30b277-1b72-43dc-8587-9104fef7cb95" />

- **Distribution of visa-sponsored roles:**  
  - Engineer: 167 roles **(dominant category)**  
  - Accountant: 143 roles  
  - Others: 141 roles  
  - Healthcare: 119 roles  
  - Assistant: 86 roles  
  - Manager: 84 roles  
  - Data roles: 77 roles  
  - Mechanical: 3 roles **(negligible demand)**  

- **Insight:**  
  - Engineering and accounting roles lead sponsorship demand.  
  - Healthcare remains a strong and consistent sector.
  - Mechanical roles show **extremely low sponsorship**, indicating either low demand or local hiring preference.  

---

### Job Platforms Offering Sponsorship Roles  
<img width="829" height="553" alt="image" src="https://github.com/user-attachments/assets/573b083e-8dbd-42ef-bc9c-8e7e70056aec" />

- **Top platforms by number of listings:**  
  - Career.zycto: 12 listings  
  - Hiring.zycto: 7 listings  
  - Indeed: 5 listings  
  - Careers.aliyucares: 5 listings  
  - Women For Hire: 4 listings  

- **Low-volume platforms (≤3 listings):**  
  - Jobs, BeBee, JobLeads, Aliyucares, Talents By Yulia  

- **Insight:**  
  - A **small number of niche platforms dominate sponsorship listings**  
  - General platforms contribute but are less targeted for sponsorship-specific roles.  

---

### Top Locations in the United Kingdom with Sponsorship
<img width="829" height="555" alt="image" src="https://github.com/user-attachments/assets/cc16acf0-7bc8-4329-9374-61b89a663484" />

- **Highest activity locations:**  
  - Aberdeen: 3 listings  
  - United Kingdom (unspecified): 3 listings  
  - Edinburgh, Liverpool, York: 2 listings each  

- **Low-frequency locations (1 listing each):**  
  - Belfast, Birmingham, Glasgow, Nottingham, Oxford, Cambridge, etc.  

- **Insight:**  
  - Opportunities are **geographically dispersed but shallow in volume**  
  - Slight clustering in key cities, but no strong regional dominance  

---

### Key Insights & Business Implications  
- Visa sponsorship is **limited and unevenly distributed**, with heavy reliance on a few job platforms.  
- Aggregator platforms (e.g., zycto) play a **critical role in surfacing opportunities**.  
- Engineering, accounting, and healthcare dominate — indicating **skill shortages in these domains**.  
- Most employers post only once, suggesting **low hiring scale for international candidates**.  
- Candidates should prioritize:  
  - High-volume platforms  
  - Engineering/technical roles  
  - Flexible location preferences for better success rates  


## **Future Improvements**

* Scrape more data from different job platforms such as LinkedIn, Indeed, and Glassdoor.
* Extract job skills by building a custom scraper, as SerpAPI does not provide detailed skill data.
* Provide recommendations for job seekers based on best roles, locations, and job platforms.

---

## **Excel Dashboard**
```
Raw Data : 
https://github.com/jagroop-dev-11/jobs_scrapper/blob/main/uk_jobs_data%20copy.xlsx

Transformed Data with Excel Dashboard :
https://github.com/jagroop-dev-11/jobs_scrapper/blob/main/uk_jobs_data.xlsx
```
