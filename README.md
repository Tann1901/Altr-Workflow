# Altr-Workflow

This repository serves as a collection of my examples and solutions for cleaning and transforming raw data into actionable insights.

## Example 1: Find date with highest total value
#### 1. Data sample
![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/16b15bbb-4503-4b04-9df8-8a516f1eca63)

#### 2. Questions
Find the employee with the shortest average time between consecutive calls during the week
Then, identify the day when this employee received the highest total value of donations.

#### 3. Work Flow
Replace null with 0, sum all value, find average duration in seconds, sum of total value and group by employee name.
After finding the Employee name with shortest average time, I sort the value descendingly and splite text of date time, and sum the value of donations by day.

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/6f9f11cd-acb6-469c-85f6-7f55400079f5)

#### 4. Answer
![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/e88aa2dd-040d-44a5-9d3e-3227ef7b18f6)

ANS 03-02

## Example 2: Find date with highest total value
#### 1. Data sample
![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/3a5faca1-e54a-4934-ba43-6d4e0e719cf2)

#### 2. Questions
HR wants to know how many employees are three levels below the CEO in the reporting structure, excluding their own level and the level of the CEO (CEO = null).

#### 3. Work Flow
I perform data cleaning, then join the Manager ID with Employee ID consecutively from top to bottom and count the employees when join finish.
![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/3c8c5ea9-a99d-497a-a504-ada878c42829)

#### 4. Answer
![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/801b70db-8537-4da1-942d-234360bcfc7e)

ANS 84

## Example 3: Find date with highest total value
#### 1. Data sample
Sales Jan-May

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/3898f7d5-ce7b-447f-a3df-becd2c2e9ff6)

Sales June

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/9a685d8a-fe32-4d8c-8894-d1a0f29ed992)

#### 2. Questions
Calculate the total sales from the ten lowest performing stores in each region in the June table.

Then combine the table with Jan-May, find out which region has the lowest sales total from Jan - June.

#### 3. Work Flow
In June data, due to data was squeezed together, I split them by the pattern. Then I divide in different regions and sum the sales, filter the top 10 of them and union, group by store.
I then transpose data to match with Jan-May format. I fill in the name of June in Month column, calculate and define the total.

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/f4cf7224-ee8f-47fd-a265-570078021ac3)

#### 4. Answer
Group by Month

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/ede7453f-c80c-469f-b136-57af1ac100e4)

Group by Store Name

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/a79ddcd9-17d4-45b4-b8a8-a669b67c1f77)

ANS D

## Example 4: Find date with highest total value
#### 1. Data sample

Single store report

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/883abdb3-36d5-41c1-8d0b-15b3b894e74e)

Multiple store report across sheets

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/9ccb3978-1abb-44e2-9ec2-27414b0e6db6)

Name standardized

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/41a88c2b-1932-4c36-9d2e-575db0891a86)

City and Store ID 

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/9e271212-b5d5-4b69-84d8-e87bf5db34b7)


#### 2. Questions
Request a report a full report of every store. However, each store's report has 4 columns but varies in column headers and order. All store reports are saved as separate sheets in the dataset. 

The dataset also includes the city where each store is located, helping to standardize column headers. 

Find Which city has the largest total sales.

#### 3. Work Flow

I created a macro for one sheet to standardized name.
The I applied macro for all of the sheets.
Then I join with the city name for inputs and sum the sales, sort it descending.

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/0e8fe11d-d85c-46c5-ad0b-7f7781e51d38)

#### 4. Answer
Macro to standardize column title across sheets 

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/bb4d7cac-adab-4630-8bb8-a86849ede0d2)

Sum Sales by City 

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/17c8b38e-ea42-4dfd-a1a7-c4d17a55da0d)

ANS Colorado Springs


## Example 5: Team member assignment
#### 1. Data sample

Team member assignment

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/33651a64-ebe0-43bb-8888-0f5d77f0006f)


#### 2. Questions
Team members will be split into 25 groups and sent to different locations to perform community service. Some of the members have already been assigned a group, but most have not.
Assign the remaining members to groups so that each group has a total of 20 volunteers.
Perform the assignment in order by member number. For example, if group 1 needs ten more volunteers, assign the first ten available volunteers to that group. The same process would repeat for group 2, then group 3, etc. until all 500 members are assigned to a group
What is the sum of the group numbers for memeber 1617, 1755, and 1870?

#### 3. Work Flow

Split the table into null and not null.
With not-null containing values, count how many values lack in each group and assign row count of remaining in each group and create an index for whole table.
With null contained values, create an index value.
Join by index value of two to match with the listing of remaining with the name of members.
Combine with original filled data.

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/30d0bd00-cab8-49b5-ba35-c0223ca08e9c)


#### 4. Answer

Assigned table 

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/b82949c2-8dc4-4220-9ed7-855e9ab525bf)

Sum of group 

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/4b41f3da-6587-42bd-a524-a05614ba6827)

![image](https://github.com/Tann1901/Altr-Workflow/assets/108020327/3f483e3b-28f4-4118-8fe7-87f237243c4c)

