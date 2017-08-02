# Get Emails From Google Form

Download your Google Form responses to \*.CSV file.

![](/assets/import.png)

Change the filenname to your CSV filename, for example "JoinPythonSharingCourses.csv" to your filename.

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

Run below code in command line and you will get those email output.

```bash
Python GetEmailFromGoogleFormCSV.py >1.txt
```





