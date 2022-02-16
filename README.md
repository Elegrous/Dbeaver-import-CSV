# How import CSV file to Dbeaver
[DBeaver](https://dbeaver.io/) - SQL client software application and a database administration tool.<br/>

Select CSV to connect to CSV database:<br/>
<img width="550" alt="image" src="https://user-images.githubusercontent.com/44158648/154039742-0d4c5e26-cf9b-4eba-b2b4-fa76b04e0ed9.png">

If date format in your CSV file is standard for DBeaver, i.e. yyyy-MM-dd, there will be no issue and you can click on Finish.

But if dates in your CSV file have formats: dd/MM/yyyy, or M/dd/yyyy, etc., need to do additional steps:

### Example
We have this Table with 30 columns:
<img width="1418" alt="image" src="https://user-images.githubusercontent.com/44158648/154260015-78f6b62d-b365-4af3-9815-ab9280fd73ec.png">

In Driver Properties add dateFormat as in the csv file, i.e. M/dd/yyyy in our example, and add columnTypes for each column.
Therefore, setting should be the following:<br/>

columnTypes: integer,integer,integer,string,integer,string,string,string,integer,string,date,date,string,string,integer,string,string,integer,integer,string,integer,float,integer,integer,integer,integer,string,date,date,string<br/>

<img width="550" alt="image" src="https://user-images.githubusercontent.com/44158648/154262402-db29dfa7-37b6-450f-bada-982542d9ba5f.png">

### Result
<img width="250" alt="image" src="https://user-images.githubusercontent.com/44158648/154263179-b6589566-d0ad-4953-9496-e87d40562c62.png">


Sourse is the issue [CSV file date format is not recognised as set in driver properties - default is used #11612](https://github.com/dbeaver/dbeaver/issues/116120)
