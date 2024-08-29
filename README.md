# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
CODE:
data cleaning
import pandas as pd df=pd.read_csv('/content/SAMPLEIDS.csv') df
![Screenshot 2024-08-29 103205](https://github.com/user-attachments/assets/f4e6252d-4f65-471f-b006-da1aeb6b03b3)
df.isnull()
![image](https://github.com/user-attachments/assets/8bb6ef90-1e45-4f59-bf91-be5be14f7cb0)
df.notnull()
![Screenshot 2024-08-29 103524](https://github.com/user-attachments/assets/823fe2bc-598c-41a8-b9ce-6c6f777f6cc3)
df.dropna(axis=1)
![Screenshot 2024-08-29 104158](https://github.com/user-attachments/assets/5f792360-f45c-42e2-8ea2-f9e0bd861e4d)
df.fillna(0)
![Screenshot 2024-08-29 104246](https://github.com/user-attachments/assets/110331ee-5270-4ed5-8f9e-075442c41cca)
df.fillna({'GENDER':'MALE','NAME':'SRI','ADDRESS':'POONAMALEE','M1':98,'M2':87,'M3':76,'M4':92,'TOTAL':305,'AVG':89.999999}
![Screenshot 2024-08-29 104340](https://github.com/user-attachments/assets/fcf3d7be-0fe1-41f5-8c61-979ec950afff)
### IQR(Inter Quartile Range)
import pandas as pd ir=pd.read_csv('/content/iris.csv') ir
![Screenshot 2024-08-29 104530](https://github.com/user-attachments/assets/45c61421-9851-456a-b250-7927f0e7a6f0)
ir.describe()
![Screenshot 2024-08-29 104649](https://github.com/user-attachments/assets/fda83827-92aa-4a2a-a8fa-384be36823d3)
rt seaborn as sns sns.boxplot(x='sepal_width',data=ir)
impo![Screenshot 2024-08-29 104755](https://github.com/user-attachments/assets/78833dbc-4786-4c92-a794-f2ffd14537e3)
pal_width.quantile(0.25) c3=ir.sepal_width.quantile(0.75) iq=c3-c1 print(c3)
c1=ir.se![Screenshot 2024-08-29 104847](https://github.com/user-attachments/assets/bebe1235-ddec-4ade-b4c3-89906ac913c1)
rid=ir[((ir.sepal_width<(c1-1.5iq))|(ir.sepal_width>(c3+1.5iq)))] rid['sepal_width']




