You have been given data and a study area of data anlaysis. 
Your next step is to write out the steps that you need to follow to get to your end goal.

Begin your process by pseudo coding out - or writing out steps in plain English - everything that you will need to do in order to get to your end goal.
The steps below will walk you through beginning this process of writing pseudocode.

Write Pseudocode
=================
# Steps required to process data analysis
::
1. Get a list of files in the directory
2. Subset the list to just the files required to data analysis
3. Devided the taks into smaller sub-task
4. Calculate and Summarize the data analysis
5. Save the clean and intermediate data for future use
::
# Produce your result/plot!


Data Workflow Best Practices
============================
There are many things to keep in mind when creating a workflow. A few include:
::
1. Do not modify the raw data
Typically you do not want to modify the raw data, so that you can always reproduce your output from the same inputs. 
In some cases, this is less important, e.g., when you are not tasked with curating the raw data.

A good rule of thumb is to create an “outputs” directory where you store outputs. An outputs directory is helpful because:
You can always delete and recreate the outputs without worrying about deleting your original data.
An outputs directory is expressive and reminds anyone looking at your project (including you in the future - i.e. your future self!) 
where the output products are - they don’t have to dig for the data.

2. Create Expressive Intermediate File Names and Outputs
You want to carefully consider how you name your intermediate and end product outputs so that the names reflect your intention and the content. 
For instance - if you are working on dataframe which would be exported to a csv.

Here are some naming options:

# Less than ideal name
data.csv
# OK Name
analysis.csv`
# Expressive name
all-sites-date.csv

3. Whenever Possible Create Modular Code

As you are working on your pseudo code, consider the parts of your analysis that are well suited for functions. 
Keep functions small and focused. A function should do one thing well. You can then combine many functions into a wrapper function to automate and make for a nicely crafted program.
::