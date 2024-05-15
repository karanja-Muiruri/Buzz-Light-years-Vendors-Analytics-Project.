# Buzz-Light-years-Vendors-Analytics-Project.

## Table of Contents
 - [Project Overview](#project-overview)
 - [Data Sources](#data-sources)
 - [Tools Used](#tools-used)
 - [Data Preparation](#data-preparation)
 - [Exploratory Data Analysis](#exploratory-data-analysis)

## Project Overview
Analysis of vendor locations for all customers that have yet to complete the repair on their Buzz Light years; for use in determining where to send the repair trucks first.

### Data Sources
The primary dataset used for this analysis;
  - 'Customer Information.csv'
  - 'Log Tracking_Completed_File_1.csv'
  - 'Log Tracking_Completed_File_2.csv'
  - 'Log Tracking_Completed_File_3.csv'
  - 'Log Tracking_Incompleted_File_1.csv'
  - 'Log Tracking_Incompleted_File_2.csv'
  - 'Log Tracking_Incompleted_File_3.csv'
  - 'Manufacturing Log.csv'
  - 'Vendor Allocation.csv'

  ### Tools Used
  - Tableau
    
 ### Data Preparation
 In the initial data preparation phase, I performed the following tasks;
 - Data Loading and Inspection.
    - Loaded all the appropriate data sets.
       - ![Dataproject1](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/069ace26-d3b6-4428-bd5e-18e0acbe455a)
    - I did a Left Join of Customer Information.csv to Vendor Allocation.csv to ensure all customers from Customer Information.csv are included as well as including state from vendor state(Vendor Allocation.csv).
       -  ![dataproject02](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/ab14384b-5c2b-4558-972b-f91bc92ffc49)
    - I then created a relationship between Customer Information.csv with Log Tacking_Completed_File_1.csv; followed by a union in Log Tracking_Completed_File_1.csv with the rest of the Log Tracking Files.
       -  ![Dataproject03](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/31e0d76b-d691-4ca2-921a-3f725b4afd3c)
      

 - Handling null and duplicate values.
    - I did a normal count and a count distinct of Customer ID (both for Customer Information and Log tracking data sets) to check for any duplicate values.
       -  ![Dataproject04](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/d26f85ad-19e3-4d21-839e-77a81691614d)
    - The Left join on Customer Information.csv to Vendor Allocation.csv is join on customer Suburb to vendor suburb as well as Customer Zip Code to Vendor Zip Code to avoid any duplicates.
       -   ![dataproject02](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/1a12def1-4015-4bd7-8381-1e87d71b255f)

   
 
 ### Exploratory Data Analysis 
 EDA involved exploring the sales data to answer key tasks, such as;
  - Analyzing the locations of the vendors for all customers that have yet to complete the repair on their Buzz Light years.
      -  Using Vendor Zip Code, I created a density map, as well as adding a Status filter that excludes COMPLETE, thus a map showing vendor zip codes with incomplete repairs.
       -   ![Dataproject06](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/6933b525-f152-4721-83fb-dd79bec53d79)

  - Removing any customers that don't have a home address.
      - I used a pie chart to indicate to the stakeholders the number of customers without a home address incase there's an update or fix needed to be done on the current dataset before removing them.
       -   ![Dataproject05](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/92b6f4f4-5be1-42c0-9b6d-c050c615895b)

  - Building a dashboard highlighting the concentrations for guidance on where to send repair trucks first.
      -  ![Dataproject07](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/57a4ea6b-d4f9-4a78-818f-1f12d88507e8)

  - Isolating customers living in the most densely populated area in the state of Victoria (Australia).
     - I used the Vendor State to create a density map, created a second map by duplicating the longitude in the columns section. I then altered the second map from density to cicle. I later applied dual axis on the second map to create a single map for better illustration. The map applies a Status filter by excluding Null and Complete values as well as a Vendor State filter showing only the state of Victoria.
       -   ![Dataproject08](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/fe6df740-7b4a-43b3-8f3a-c65a810b9411)
       -   ![Dataproject09](https://github.com/karanja-Muiruri/Buzz-Light-years-Vendors-Analytics-Project./assets/169806532/89bcd76f-3055-442c-acf2-e2019fd1f10d)


  - Showing the models originally purchased by these customers.
       - I added the Manufacturing Log.csv as a relationship to the Customer Information.csv to include




  





