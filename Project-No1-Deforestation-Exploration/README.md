## Project Overview

You’re a data analyst for **ForestQuery,** a non-profit organization. on a mission to reduce deforestation around the world and which raises awareness about this important environmental topic.

Your executive director and her leadership team members are looking to understand which countries and regions around the world seem to have forests that have been shrinking in size, and also which countries and regions have the most significant forest area, both in terms of amount and percent of total area. The hope is that these findings can help inform initiatives, communications, and personnel allocation to achieve the largest impact with the precious few resources that the organization has at its disposal.

You’ve been able to find tables of data online dealing with forestation as well as total land area and region groupings, and you’ve brought these tables together into a database that you’d like to query to answer some of the most important questions in preparation for a meeting with the ForestQuery executive team coming up in a few days. Ahead of the meeting, you’d like to prepare and disseminate a report for the leadership team that uses complete sentences to help them understand the global deforestation overview between 1990 and 2016.

## Project walkthrough ##

  1. I Created a **View** called **“forestation”** by joining all three tables - **forest_area, land_area** and **regions**.
  2. I *Joined* **forest_area** and **land_area** tables on both **country_code** AND **year**.
  3. I *Joined* **regions** table to the above two based on only **country_code**.
  4. In the ‘forestation’ View, I included the following:
   *  **All of the columns of the origin tables**
   *  A **new column** that provides the **percent of the land area that is designated as forest.**
  5. Because the column **forest_area_sqkm** in the forest_area table and the **land_area_sqmi** in the land_area table were in **different units (square kilometers   and square miles, respectively),** an adjustment was needed to be made in the calculation based on the following 1 sq mi = 2.59 sq km.


***I then created a report for the executive team in which I explained my results.***

## Report Sections ##

The report has five sections:

  1. Global Situation
  2. Regional Outlook
  3. Country-Level Detail
  4. Recommendations
  5. Appendix: SQL queries used

*It was completed answering the following questions:*

## 1. GLOBAL SITUATION ##

a. What was the total forest area (in sq km) of the world in 1990? Please keep in mind that you can use the country record denoted as “World" in the region table.

b. What was the total forest area (in sq km) of the world in 2016? Please keep in mind that you can use the country record in the table is denoted as “World.”

c. What was the change (in sq km) in the forest area of the world from 1990 to 2016?

d. What was the percent change in forest area of the world between 1990 and 2016?

e. If you compare the amount of forest area lost between 1990 and 2016, to which country's total area in 2016 is it closest to?

## 2. REGIONAL OUTLOOK ##

*Here I first created a table that shows the Regions and their percent forest area (sum of forest area divided by sum of land area) in 1990 and 2016. (1 sq mi = 2.59 sq km).*

Based on this table the questions answered were...

a. What was the percent forest of the entire world in 2016? Which region had the HIGHEST percent forest in 2016, and which had the LOWEST, to 2 decimal places?

b. What was the percent forest of the entire world in 1990? Which region had the HIGHEST percent forest in 1990, and which had the LOWEST, to 2 decimal places?

c. Based on the table you created, which regions of the world DECREASED in forest area from 1990 to 2016?

## 3. COUNTRY-LEVEL DETAIL ##

a. Which 5 countries saw the largest amount decrease in forest area from 1990 to 2016? What was the difference in forest area for each?

b. Which 5 countries saw the largest percent decrease in forest area from 1990 to 2016? What was the percent change to 2 decimal places for each?

c. If countries were grouped by percent forestation in quartiles, which group had the most countries in it in 2016?

d. List all of the countries that were in the 4th quartile (percent forest > 75%) in 2016.

e. How many countries had a percent forestation higher than the United States in 2016?
