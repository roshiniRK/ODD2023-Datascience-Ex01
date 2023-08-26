# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE :
### Data_set.csv :
```
import pandas as pd
import numpy as np
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('Data_set.csv')
df.info()
df.head()
df=df.dropna(subset=['show_name'])
df.head()
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].median())
df.head()
df=df.dropna(subset=['current_overall_rank'])
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].mean())
df.head()
df.info()
```
### Loan_data.csv :
```
import pandas as pd
import numpy as np
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('Loan_data.csv')
df.info()
df.head()
df['Gender']=df['Gender'].fillna('Female')
df.head()
df['Dependents']=df['Dependents'].fillna(method='ffill')
df.head()
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.head()
df=df.dropna(subset=['LoanAmount'])
df.head()
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].min())
df.head()
df.info()
```
# Output:
## Data_set.csv:
### Non Null Before:
![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/d48c921c-92c2-4b75-bde5-856037fa4bb6)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/7fd7f1f9-6562-4a79-80eb-ef87e4973d41)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/cd299d6f-242d-4dce-a1b3-ddf4370ef812)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/a0f64268-2b9d-4b17-9ebf-2949b7e4998d)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/b86910e9-ca53-48b6-904d-f8bbdae29c0a)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/eb0c1062-24ae-4d0b-9df1-83a96d7c61a1)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/ae581952-649f-4cc6-9337-3f9033a13bcc)

### Non Null After:

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/5cf9fac4-bba3-44e1-bf2c-c93f51af1cfc)

## Loan_data.csv:

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/a6c4ae97-dbbc-4a71-807f-7daf100479ef)


![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/818e5080-b804-4f33-84eb-123b5fcee17f)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/8bd4447a-e745-43f0-bb55-6958c3ebb548)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/2588829b-104a-4471-8cb0-5cc12e7fbb32)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/e250f544-dc31-4683-90b6-d1f1254afa8c)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/43e4cb50-1e28-4731-8a37-ad4d2937a730)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/0dd7fc27-9b5c-4ba2-8480-ddc1a755540c)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/27350604-ff32-438e-9717-59e18c1887c7)

![image](https://github.com/roshiniRK/ODD2023-Datascience-Ex01/assets/118956165/6310fc05-1be1-47a3-9768-094a0533d0a2)
















