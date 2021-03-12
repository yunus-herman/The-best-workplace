# Capstone Project - The Best Place to Work 

**by : Yunus Herman**

**Software Requirements:**
- Google Chrome
- HTML
- XPath
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Selenium
- Scikit-learn
- StandardScaler
    
## Table of Contents:

For our audience, please begin by examining our ReadMe and read the Introduction, Problem Statement, and Background to familiarize yourselves with the design and focus of our project. Then refer to the below ordered notebooks (01_Glassdoor_Scraping.ipynb, 02_Data_Cleaning_EDA.ipynb &    03_Modeling.ipynb). Then you should be able to proceed with the remaining sections of our Readme detailing our process, and finally our Executive Summary/Recommendations can be found on Readme file.   

## Notebooks:

- 01_Glassdoor_Scraping.ipynb

- 02_Data_Cleaning_EDA.ipynb

- 03_Modeling.ipynb


## Executive Summary:

- README.md

## Data:

- companies.csv



## Introduction:

This project will be presenting to job seekers regarding to seek the best place to work. For employers, this project will be presenting 'how to boost company rating'. 

## Problem Statment:

Can we use company data (size, revenue, founded, jobs posted) and benefits to predict employee satisfaction? What kind of benefits that make company more attractive to job seeker? 

## Background:

Everyday there are a story about complain and stress in a work. But also we hear about a great experience in a work....  

## Data Retrieval:

Data from web scraping with Selenium of sources :
**Glassdoor.com**

Web scraping code : **01_Glassdoor_Scraping.ipynb**
 

### Data Dictionary:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|name|object|companies|Name of company|
|industry|object|companies|Industry of company|
|office|object|companies|Number of offices or branch of company, null means 1 office |
|review_counts|object|companies|Number of reviews on Glassdoor.com |
|salaries_counts|object|companies|Number of employees have shared their salaries on Glassdoor|
|jobs_count|object|companies|Number of jobs posted|
|interviews_count|object|companies|Number of interview reviews|
|benefits_count|object|companies|Number of benefit reviews|
|website|object|companies|Website of  company|
|company_type|object|companies|Company's type|
|revenue|object|companies|Company's revenue|
|head_quarter|object|companies|Company's headquarter|
|founded|float|companies|Company founded year|
|interview_possitive|object|companies|Number of possitive interview experience in %|
|interview_negative|object|companies|Number of negative interview experience in %|
|interview_neutral|object|companies|Number of neutral interview experience in %|
|interview_difficulty|float|companies|Interview difficulty 1 - 5 (easy - hard)|
|benefits_score|float|companies|Benefits rating 1-5 (bad - good)|
|rating|float|companies|Company's rating 1-5 (bad - good)|
|total_insurance_health_wellness_benefits|int|companies|Total insurance, health, and wellness benefits (0 - 13)|
|health_insurance|int|companies|Has health insurance (0 - no, 1 - yes)|
|dental_insurance|int|companies|Has dental insurance (0 - no, 1 - yes)|
|FSA|int|companies|Has Flexible Spending Account (FSA) (0 - no, 1 - yes)|
|vision_insurance|int|companies|Has vision insurance (0 - no, 1 - yes)|
|Health Savings Account (HSA)|int|companies|Has Health Savings Account (HSA) (0 - no, 1 - yes)|
|life_insurance|int|companies|Has life insurance (0 - no, 1 - yes)|
|supplemental_life_insurance|int|companies|Has supplemental life insurance (0 - no, 1 - yes)|
|disability_insurance|int|companies|Has disability insurance (0 - no, 1 - yes)|
|occupational_accident_insurance|int|companies|Has occupational accident insurance  (0 - no, 1 - yes)|
|health_care_on_site|int|companies|Has health care on site (0 - no, 1 - yes)|
|mental_health_care|int|companies|Has mental health care (0 - no, 1 - yes)|
|retiree_health_and_medical|int|companies|Has retiree health and medical (0 - no, 1 - yes)|
|accidental_death_and_dismemberment_insurance|int|companies|Has accidental death and dismemberment insurance (0 - no, 1 - yes)|
|total_financial_retirement_benefits|int|companies|Total benefits in financial retirement category (0 - 9)|
|pension_insurance|int|companies|Has pension insurance (0 - no, 1 - yes)|
|plan_401k|int|companies|Has 401k plan (0 - no, 1 - yes)|
|retirement_plan|int|companies|Has retirement plan (0 - no, 1 - yes)|
|employee_stock_purcase_plan|int|companies|Has employee stock purcase plan (0 - no, 1 - yes)|
|performance_bonus|int|companies|Has performance bonus (0 - no, 1 - yes)|
|stock_options|int|companies|Has stock options/ offering (0 - no, 1 - yes)|
|equity_incentive_plan|int|companies|Has equity incentive plan (0 - no, 1 - yes)|
|supplemental_workers_compensation|int|companies|Has supplemental workers compensation (0 - no, 1 - yes)|
|charity_gift_matching|int|companies|Has stock charity gift matching (0 - no, 1 - yes)|
|total_family_parenting_benefits|int|companies|Total benefits  in family parenting category (0 - 10|
|maternity_paternity_leave|int|companies|Has maternity paternity leave (0 - no, 1 - yes)|
|work_from_home|int|companies|Has work from home (0 - no, 1 - yes)|
|fertility_assistance|int|companies|Has fertility assistance (0 - no, 1 - yes)|
|dependent_care|int|companies|Has dependent care (0 - no, 1 - yes)|
|adoption_assistance|int|companies|Has adoption assistance (0 - no, 1 - yes)|
|childcare|int|companies|Has childcare (0 - no, 1 - yes)|
|flexible_hour|int|companies|Has flexible working hour (0 - no, 1 - yes)|
|military_leave|int|companies|Has military leave (0 - no, 1 - yes)|
|family_medical_leave|int|companies|Has family medical leave (0 - no, 1 - yes)|
|unpaid_extended_leave|int|companies|Has unpaid extended leave (0 - no, 1 - yes)|
|total_vacation_time_off_benefits|int|companies|Total benefits in vacation time off category (0 - 6)|
|vacation_paid_time_off|int|companies|Has vacation paid time off (0 - no, 1 - yes)|
|sick_days|int|companies|Has sick days (0 - no, 1 - yes)|
|paid_holidays|int|companies|Has paid holidays (0 - no, 1 - yes)|
|volunteer_time_off|int|companies|Has volunteer time off (0 - no, 1 - yes)|
|sabbatical|int|companies|Has sabbatical (0 - no, 1 - yes)|
|bereavement_leave|int|companies|bereavement leave (0 - no, 1 - yes)|
|total_perk_discounts_benefits|int|companies|Total benefits in perk discounts category(0 - 11)|
|employee_discount|int|companies|Has employee discount (0 - no, 1 - yes)|
|free_lunch_or_snacks|int|companies|Has free lunch or snacks (0 - no, 1 - yes)|
|employee_assistance_program|int|companies|Has employee assistance program (0 - no, 1 - yes)|
|gym_membership|int|companies|Has gym_membership (0 - no, 1 - yes)|
|commuter_checks_and_assistance|int|companies|Has commuter checks and assistance (0 - no, 1 - yes)|
|pet_friendly_worksplace|int|companies|Has pet friendly worksplace (0 - no, 1 - yes)|
|mobile_phone_discount|int|companies|Has mobile phone discount (0 - no, 1 - yes)|
|company_car|int|companies|Has company_car (0 - no, 1 - yes)|
|company_social_events|int|companies|Has company social events (0 - no, 1 - yes)|
|travel_concierge|int|companies|Has travel concierge (0 - no, 1 - yes)|
|legal_assistance|int|companies|Has legal assistance (0 - no, 1 - yes)|
|total_professional_support_benefits|int|companies|Total benefitss in professional support category (0 - 5)|
|diversity_program|int|companies|Has diversity program (0 - no, 1 - yes)|
|job_training|int|companies|Has job training (0 - no, 1 - yes)|
|professional_development|int|companies|Has professional_development (0 - no, 1 - yes)|
|apprenticeship|int|companies|Has apprenticeship (0 - no, 1 - yes)|
|tuition_assistance|int|companies|Has tuition_assistance (0 - no, 1 - yes)|


### Web Scraping: 

First thing to do was searching about which website has the data that I need for the project. I found Glassdoor.com has a lot of company reviews, features, great data quality and detail, and also has a large number of companies in the USA. This website is one of the best for job searching and job posting for employers. 
After I explored the website to get the insight of the website structure, I made a list of which features that I want to get. 
 
I use Selenium and get elements with the Xpath selector. Get element(s) by Xpath has a better successful rate than other methods. I prefer Selenium than BeautifulSoup for this website because of the same reason. Google Chrome setted as my web scraping PATH. I use this browser to inspect elements in HTML and trace the target data. 
Data collected in Dictionary format and then pandas dataframe. Lastly I store the data into a csv file named companies.csv in the data folder for the next step, data cleaning and Evaluation Data Analysis.



### Data Cleaning:

One thing I wanted to do was check and remove all duplicates because the data scraping process was on and off several times. I checked null values from all feature columns. Some null mean something, for example, if the office column is null means no branch (1 office only). Column types were checked and converted into numeric if do-able, for example string 6.6k means 6.6 x 1000 = 6600. 
Some columns, for example, Company size column has been converted into 3 numerical categories: 
1 - less than 5000 employees
2 - 5001 to 10000 employees
3 - 10000+ employees 
 
The most important feature is company rating in the form of 1 to 5 and in 1 decimal digit. I used this to determine companies are great, good or below average (3,2 or 1). This feature is the target of modeling. I call this as company rank feature.  


### EDA:
Findings:

1. The more difficult company interview, company rank is better.

2. Gym membership and work from home benefits can raise company's rank

3. Company with 100 to 500 million (USD) revenue has the best rank. The bigger company revenue, has worse rank     

4. Smaller companies have the best rank (less than 5000 employee)

5. Education, Real estate, construction, non-profit, biotech & pharmaceuticals companies are the top 5 ranks.


### Modeling:

For modeling purposes, since my target is classification, I tried Random forest, SVC, Ada boost, Logistic Regression, Decicion tree, Extra tree and K-NN. I had not so good score, the best score was 0.52 with Random forest.   


**Modeling Takeaways:**
The model is not good enough to predict company's rank.

### Executive Summary:

**Problem Statement:** Can we use company data (size, revenue, founded, jobs posted) and benefits to predict employee satisfaction? What kind of benefits that make company more attractive to job seeker? 

**Recommendations:** As I have expressed throughout this notebook, I believe that I am not able to predict the employee statisfaction from benefits features. Employee statisfaction is really subjective. The measurement should be by reviews. 

I reccomend that employer can add some benefits that has positive correlation with company's rank :
- Gym membership as additional benefits, maybe it helps employee to reduce stress and healthier. 
- Allow employee to work from home, especialy during the pandemic.
- Additional health care on site can also make employee feel more secure.
- Free lunch or snacks can be an important benefit to boost company's rank.  


