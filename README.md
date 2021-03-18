  # Capstone Project - The Best to Workplace 

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
    

## Notebooks:

- 01_Glassdoor_Scraping.ipynb

- 02_Data_Cleaning_EDA.ipynb

- 03_Modeling.ipynb


## Executive Summary:

- README.md

## Data:

- companies.csv



## Introduction:

This project aims to help job seekers identify the best companies to apply at, as well as to help employers determine how to make their employees happier and simultaneously attract a large number of job applicants. To achieve these aims, the project utilizes employee reviews posted on Glassdoor, a website where current and former employees anonymously review companies. Glassdoor also allows users to apply for jobs on its platform, which makes it popular. It is widely considered to have the most accurate and comprehensive employee reviews. Therefore my project has a double aim. On the one hand, I endeavor to help job seekers like me identify the best companies to apply at. On the other hand, I also help employers determine how to make their employees happier and simultaneously attract a large number of job applicants. To achieve these aims, I used employee reviews posted on Glassdoor, and combined them with other basic data about the company, such as size (number of employees), revenue, and age (the year the company was founded. I also looked at the various benefits that each company offers, such as health insurance, 401k, gym membership, free meals, and many others.

## Problem Statement:

1. Can we use basic company data (such as size, revenue, and foundation year) and benefits offered to predict employee satisfaction? 
2. What kinds of benefits make a company more attractive to job seekers? 

## Background:

There are thousands of job ads out there - how do I know which is the right one for me? More specifically, how can I tell if I would be happy and satisfied working for a particular company?  You cannot possibly apply to all those positions, so you ask yourself: “How can I know in advance what would be the best workplaces for me?”  This is what my project is all about. Using machine learning and basic data on companies and the benefits they provide, I determined whether a company is a good workplace.  

## Data Retrieval:

Data from web scraping with Selenium of sources :
**Glassdoor.com**

Web scraping notebook : **01_Glassdoor_Scraping.ipynb**

Data of collection : March 10, 2021
 

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

I obtained my data by web scraping with Selenium from Glassdoor.com. Before getting started, I checked the robots.txt of the website to see what kinds of data I was allowed to scrape and the various rules and regulations that the company sets for data scrapers like me. Luckily, Glassdoor's policy is fairly liberal and allowed me to extract all the data I need for my study. Next I checked the website's structure and architecture (sitemap) to see what information was displayed on each page. Then I inspected the html elements of the website and determined the xpath to get the links and texts I needed. I always use find_element_by_xpath because in my experience it has the highest success rate. I then carefully tested each link and text one by one to make sure that I was getting the right results. I created a function to sort and store the data by company. I carried out quality assurance by taking some data samples and compared them to the data on the respective websites, e.g. company name, location of headquarters, how many branch offices/other locations the company has, the number of employees working for the company, and the company's revenue in the last fiscal year. Most of the features I used consisted of benefits, though.

Data collected in Dictionary format and then pandas dataframe. Lastly I store the data into a csv file named companies.csv in the data folder for the next step, data cleaning and Evaluation Data Analysis.


### Data Cleaning:

After I had obtained all the data I needed, I cleaned up the data and analyzed them. I checked if there were any nulls and converted the data to numeric values. One thing I wanted to do was check and remove all duplicates because the data scraping process was on and off several times. I checked null values from all feature columns. Some null mean something, for example, if the office column is null means no branch (1 office only). Column types were checked and converted into numeric if do-able, for example string 6.6k means 6.6 x 1000 = 6600. another example, I gave companies with over 10,000 employees the numeric value 3, companies with 5,001–10,000 employees the value 2, and companies with up to 5,000 employees the value 1.
 
Reviews on Glassdoor use the usual 1–5 rating system, including fractions (e.g. 3.4, 4.7). In order to make that manageable, I divided the ratings into three classes: 2 for above average ratings (4.3 and over), 1 for average ratings (4.0–4.2), and 0 for below average ratings (3.9 and below). This might seem mathematically strange - why is anything below 4 considered below average? The reason was that I discovered that few if any employees rated their companies below 3; the median rating was about 4.0.

### EDA:

Arguably the most interesting finding was that companies that had the toughest interviews were also the ones ranked highest.

So much for potential employees. How about the employers? What can they do in order to make their employees happier and increase their company's ranking, thus attracting the best applicants? It turned out that paid gym memberships were the most popular benefit, meaning that companies that offered this benefit ranked highest. Next came the option of working from home, which employees seem to like, although this may have changed since the advent of Covid-19. Healthcare on site was the third most popular benefit, followed by free lunch and/or snacks, and then sabbatical (which may be the reason why the education sector was overall the industry with the happiest employees). The benefits that contributed the least to the employees' satisfaction were the availability of bereavement leaves, military leaves (not sure what that means), employee discounts, family medical leave, and supplemental workers' compensation. Having a pet-friendly workplace also did not turn out to boost a company's rating. I wonder why…  

The industry (type of business the company engages in) also turned out to be significant. The education sector turned out to have the  happiest employees, followed by real estate companies, construction companies, nonprofits, and biotech & pharmaceutical companies. The least satisfied employees work in retail, followed by transportation & logistics; restaurants, bars, & food services; insurance; and business services. You're probably wondering about the ranking of IT companies: there were ranked as the 7th best industry to work in, out of 23.


### Modeling:

For modeling purposes, since my target is classification problem, I tried Random forest, SVC, ADA boost, Logistic Regression, Decicion tree, Extra tree, K-NN and Gradient Boost. The best model for this case is Gradient Boost Classifier, this model has an accuracy rate of 55%. This seem low but is nevertheless statistacally significant, because the baseline is 36%. The model is not so good at predicting a satisfaction levels of the 'average' class but is fairly accurate for the above average and below average classes.


### Recommendations:
Normally the benefits considered most important for employees are healthcare and pension 401k. Interestingly, the result of my analysis indicate that other features have a much higher predictive value when it comes to employee satisfaction. 

To improve the model, results would be more robust if companies are divided into just two classes: 'above average' and 'below average'. We should bear in mind that employee satisfaction is a highly subjective notion. Find the way to obtain data about other importance features such as salary range. 


