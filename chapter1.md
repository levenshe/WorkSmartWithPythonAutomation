# Get Emails From Google Form

Download your Google Form responses to \*.CSV, for example "JoinPythonSharingCourses.csv"

```py
import pandas as pd
CSVInputFile='JoinPythonSharingCourses.csv'
df=pd.read_csv(CSVInputFile)
print('CSVInputFile=',CSVInputFile)
print(type(df))

Emails=df.Username
print(type(Emails))

ls=Emails.tolist()
print(ls)

Emails.to_csv('out.csv', encoding='utf-8');

ss=str(ls)
ss=ss.replace("'",'')
ss=ss.replace("[",'')
ss=ss.replace("]",'')
print(type(ss))
print(ss)
```





