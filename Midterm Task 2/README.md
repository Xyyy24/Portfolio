# 𝑀𝒾𝒹𝓉𝑒𝓇𝓂 𝐿𝒶𝒷 𝒯𝒶𝓈𝓀 𝟤: 𝒟𝒶𝓉𝒶 𝒞𝓁𝑒𝒶𝓃𝒾𝓃𝑔 𝒶𝓃𝒹 𝒯𝓇𝒶𝓃𝓈𝒻𝑜𝓇𝓂𝒶𝓉𝒾𝑜𝓃 𝒰𝓈𝒾𝓃𝑔 𝒫𝑜𝓌𝑒𝓇 𝒬𝓊𝑒𝓇𝓎 𝐸𝒹𝒾𝓉𝑜𝓇
## Task Description: 
To extract useful information from the file UncleanedDSJObs.csv taken from a Job Posting site available in Kaggle.  
## To find out:
Which Job Roles pay the highest and least
What size companies pay the best
Where Job Roles or Job Titles pay the best and least in a specific state
## Dataset Before Cleaning and Transformation:
[Uncleaned DS Jobs](https://github.com/rxnz03/EDM-Portfolio/blob/main/Midterm%20Lab%20Task%202/Uncleaned_DS_jobs.csv)

## Steps Performed in Data Cleaning and Transformation:
Duplicated the raw data to preserve the original.  
Cleaned the salary estimate column by removing everything after the "(" symbol.  
Created Min Sal and Max Sal columns from the salary estimate.  
Added a new column Role Type to classify jobs as "data scientist", "data analyst", "data engineer", "machine learning engineer", or "other" based on the job title.  
Corrected the location column with custom states and split it into city and state abbreviation.  
Replaced incorrect state entries (e.g., "anne rundell" to "ma").  
Split the company size column to extract MinCompanySize and MaxCompanySize, and removed the word "employees".  
Replaced invalid or negative values:  
Competitors: replaced -1 with "n/a".  
Revenue: replaced negatives with 0.  
Industry: replaced -1 with "other".  
Cleaned company name by removing extra ratings or numbers at the end.  
Removed unnecessary columns like job descriptions.  
Duplicated the cleaned data as Sal By Role Type dup, selected Role Type, Min Sal, and Max Sal, converted salaries to currency, multiplied by 1000, and grouped by - Role Type to get average salaries.  
Created a reference as Sal By Role Size ref, selected Size, Min Sal, and Max Sal, multiplied salaries by 1000, and grouped by Size to get average salaries.  
Imported a State Mapping file to map state abbreviations to full state names and merged it with the dataset.  
Created a reference as Sal By State ref, selected State Full Name, Min Sal, and Max Sal, multiplied salaries by 1000, and grouped by State Full Name to get average salaries.  
Checked query dependencies to confirm correct relationships.  

## Final Output
### Cleaned Data


### Sal By Role Type Dup
![02](https://github.com/user-attachments/assets/813828ae-153c-40df-85f2-1dc2a421e3c6)


### Sal By Role Size Ref
![03](https://github.com/user-attachments/assets/4f7f9370-c2ac-4db5-88f7-ca13b170e17f)


### Sal By State Ref
![05](https://github.com/user-attachments/assets/918d9573-db3e-44fa-a23a-21cb714f3b09)


### Query Dependencies
![final](https://github.com/user-attachments/assets/b316355e-d1c9-4b41-b183-e17fe2c1638e)

