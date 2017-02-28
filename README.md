# edX--MSDS-Curriculum--DAT206x
for DAT206x Analyzing and Visualizing Data with Excel course on edX as part of the Microsoft Data Science curriculum
[DAT206x Analyzing and Visualizing Data with Excel](https://courses.edx.org/courses/course-v1:Microsoft+DAT206x+1T2017/)

Excel is one of the most widely used solutions for analyzing and visualizing data. Beginning with Excel 2010, new tools were introduced to enable the analysis of more data, to improve visualizations and to enable more sophisticated business logic.

In this course, you will learn about latest versions of these tools in Excel 2016. You will see how to import data from different sources, create mashups between data sources, and prepare the data for analysis. You will learn about how business calculations—from simple to more advanced—can be expressed using the DAX calculation engine. You will also learn how the data can be visualized in Excel and shared to the Power BI cloud service.

The course is designed for self-paced study of around 2-4 hours per week for six weeks, including lectures, quizzes, labs and further readings. All quizzes and lab exercises are graded. The quizzes account for 30% of the total grade, the lab exercises accounts for 65% of the total grade, and the mandatory survey accounts for the remaining 5%. You must achieve an overall score of 70% to pass the course.

## Course Outline
### Module 1: Data Analysis in Excel
- Perform data analysis in Excel using classic tools, such as VLOOKUP function, pivot tables, pivot charts, and slicers, on data that is already in a worksheet / grid data.
  - Use VLOOKUP to combine data into one range.
  - Connect a slicer with pivot tables and pivot charts components.
  - Conditionally format cells.

#### Lab 1: Explore and Extend a Classic Excel Dashboard
See the "Dashboard - CA" worksheet, showing six pivot charts of different types, with associated slicers to filter the data. Play around with the slicers to select different filters and see how your choices affect the charts. Unhide the hidden worksheets to view the data source of the charts.
- Exercise 1: Explore the Classic Excel Dashboard
-  Exercise 2: Extend the Classic Excel Dashboard

----
### Module 2: The Excel Data Model
- Build a Excel Data Model from a single flat table
  - use queries (Power Query add-in in Excel 2013 and Excel 2010)
  - create a calculated column on a table in Excel Data Model
- Manage Excel Data Model
  - Diagram view of Excel Data Model
  - Types of relationships supported in the Excel Data Model
- Basic Data Analysis Expressions (DAX)
  - use DAX in Calculated columns
  - use DAX in Measures (in Excel 2013, measures are called calculated fields)
  > Measure (in Excel) is A calculation that you create for the purpose of measuring an outcome or result relative to other factors.

  - create implicit measures
  > An implicit measure is one that Excel generates for you when you add fields to the Values area of a pivot table.

  - create explicit measures
  > An explicit measure is one that you create manually using e.g. DAX.

  - RELATED function (DAX)
  > RELATED function (DAX) returns a single value that is related to the current row from another table.


#### Lab 2: Explore an Excel Data Model
In this lab, you will explore an Excel workbook that has a data model loaded into it. You will also create calculated columns in the data model, apply formatting, and create implicit and explicit measures. You will then use the data model to create pivot tables and perform some analysis with the data.
- Exercise 1: Explore the Excel Data Model
- Exercise 2: Create a Pivot Table
- Exercise 3: Create Measures

----
### Module 3:  Importing Data from a CSV File to Data Model (a PDF using Flash Fill)
- Importing Data from a CSV / XML File to Data Model
  - data pre-processing steps recorded in the Query Editor: Remove columns, Split column, Replace values

- Remarks on Using Excel 2010 to import data
  > In Excel 2010, you cannot bring the data directly to Power Pivot using Power Query. When you import data using Power Query, you can either import to Excel worksheet or only create a connection. And then, from the Power Pivot ribbon you can use Create Linked Table to add the table to the Power Pivot model.

- Importing Data from a PDF to Data Model using Flash Fill
  > To learn more about Flash Fill, check out the following resource: https://support.office.com/en-za/article/Flash-Fill-3fb96b4a-ee83-4493-af45-6522324477bd


#### Lab 3: Importing Data from a CSV File
In this lab, you will import data to Excel from a flat csv file. You will perform pre-processing steps with the data prior to loading it into Excel.
- Exercise 1: Import Data from a CSV File
- Exercise 2: Create Pivot Table(s) to Perform Analysis

----
### Module 4: Importing Data from Databases
- Importing Data from Databases
  - import multiple tables from a SQL database, and create an Excel data model from the imported data
  - data sources included as built-in options for queries (e.g. SharePoint list, Hadoop file, Active Directory, Salesforce Objects)
- Importing Data from Multiple Files
  - initial step you need to do in the Query Editor before loading the data into the Excel data model
  > Filter the header from the three other CSV files.

- Creating and using a Calendar Table in a data model
  - Two ways to create a calendar table in Excel 2016:
    - New Date Table function from the Design tab of the Power Pivot for Excel window
    - create a calendar table in the worksheet and add it to the Excel data model
  - Purposes of using a calendar table in a data model:
    - filter data by year, month, or week
    - perform advanced calculations such as year-over-year comparison

#### Lab 4: Creating Mash-ups of Data from Multiple Sources
This lab comprises of three exercises:
In the first exercise, you will import data to Microsoft Excel from a SQL database on Azure. Once you have imported the data, you will explore existing table relationships and create a new one yourself.
In the second exercise, you will import data from CSV files which resides in a file folder. You will append this new data to the corresponding existing data that comes from the SQL Database.
In the third exercise, you will create a Date table in the data model to be used for data analysis.
-  Exercise 1: Import Data from SQL Database and Create Table Relationship
- Exercise 2: Import Data from a Folder Containing CSV Files
- Exercise 3: Create a Date Table

----
### Module 5: Creating and Formatting Measures
- Creating and Formatting Measures using DAX functions
  - [SUM function](https://msdn.microsoft.com/en-us/library/ee634387.aspx)

    > e.g. fx_Total_Revenue:= SUM(FactInternetSales[Revenue]))]

  - [SUMX function](https://support.office.com/en-us/article/SUMX-Function-DAX-9ca68d1f-34cd-4a98-bc5c-36646118811a?ui=en-US&rs=en-US&ad=US)

    > e.g. fx_Total_Revenue:= SUMX(FactInternetSales, FactInternetSales[Quantity] * FactInternetSales[List Price])

  - [CALCULATE function](https://support.office.com/en-us/article/CALCULATE-Function-DAX-19654BC2-AA88-4F6C-A0B9-6FA7A59C4432)

    > e.g. fx_TotRevenue_OnlyVanArsdelSale:=  CALCULATE([TotalRevenue], Manufacturer[Manufacturer]=”VanArsdel”)

  - [DIVIDE function](https://support.office.com/en-us/article/DIVIDE-Function-DAX-515D058C-7160-49D2-B066-E220C2577D91)

    > fx_TotalUnits_Var_% := DIVIDE([Total Units Var], [LY Total Units])

- Using Advanced DAX Functions
  - [ALL function]( https://support.office.com/en-us/article/ALL-Function-DAX-331FABFC-FE7A-4072-90D1-9DECBE831C89)
  - [SAMEPERIODLASTYEAR function]( https://support.office.com/en-gb/article/SAMEPERIODLASTYEAR-Function-DAX-b8f7f423-22f5-470f-abd3-b76a1250bcc1)
  - [PREVIOUSQUARTER function](https://support.office.com/en-US/article/PREVIOUSQUARTER-Function-DAX-D6DD1BA0-0541-4C03-B928-F6884078E736)
  - [RELATED function](https://support.office.com/en-US/article/RELATED-Function-DAX-5D0EEE69-8ACD-4C3E-A0AF-FF23BA01A7BF)
  - [TOTALYTD function](https://support.office.com/en-US/article/TOTALYTD-Function-DAX-E2E45CB6-C882-4F84-A8B5-F3FFAAE27320)

#### Lab 5:
In this lab, you will write several DAX expressions to create measures to be used to analyze VanArsdel’s sales data. Specifically, you will create the following measures:
- Total Sales: calculates the total sales.
- LY Sales: calculates last year sales.
- Sales Var: calculates sales variance between this year and last year sales.
- Sales Var %: calculates sales variance between this year and last year sales in percentage.
- YTD Sales: calculates YTD sales.
- LY YTD Sales: calculates last year YTD sales.
- YTD Sales Var: calculates sales variance between this year and last year YTD sales.
- YTD Sales Var %: calculates sales variance between this year and last year YTD sales in percentage.
- Total VanArsdel Sales: calculates sales for VanArsdel manufactured goods.
- % Sales Market Share: calculates the percentage of VanArsdel manufactured goods from the total sales.

Exercises:
- Exercise 1: Last Year Comparison
  > Total Units: Total Units:=SUM([Units])

  > LY Total Units: LY Total Units:=CALCULATE([Total Units],SAMEPERIODLASTYEAR('Calendar'[Date]))

  > Total Units Var: Total Units Var:=[Total Units]-[LY Total Units]

  > Total Units Var %: Total Units Var %:=DIVIDE([Total Units Var],[LY Total Units])

- Exercise 2: Year to Date
  > YTD Total Units: YTD Total Units:=TOTALYTD([Total Units],'Calendar'[Date])

  > LY YTD Total Units: LY YTD Total Units:=CALCULATE([YTD Total Units],SAMEPERIODLASTYEAR('Calendar'[Date]))

  > YTD Total Units Var: YTD Total Units Var:=[YTD Total Units]-[LY YTD Total Units]

  > YTD Total Units Var %: YTD Total Units Var %:=DIVIDE([YTD Total Units Var],[LY YTD Total Units])

- Exercise 3: Own Brand (VanArsdel) Sale  Market Share
  > Total OwnBrand Units: Total VanArsdel Units:=CALCULATE([Total Units], Manufacturer[Manufacturer]="VanArsdel")

  > % OwnBrand Units Market Share: % Units Market Share:=IF([Total VanArsdel Units]=0, 0, DIVIDE([Total VanArsdel Units], [Total Units], 0))

----
### Module 6:

#### Lab 6:

----
### Module 7:

#### Lab 7:

----
### Module 8:

#### Lab 8:

----
## My notes

Course Progress for Student 'achoczaj'

Your enrollment: Audit track

Course start: 2017.02.20

Course end: 2017.

Course progress: Total result = %
