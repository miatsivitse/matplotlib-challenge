# matplotlib-challenge

Background:

You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

Analysis:

- The data indicates that the drugs Ramicane and Capomulin are the most effective in reducing Tumor Volume (mm3). 

- There were no outliers for Capomulin, Ramicane, or Ceftamin. Infubinol was the only drug with an outlier.

- The Capmulin drug was less effective as the mouse's weight increased.

- 51% of mice tested were male, compared to 49% female mice.

Process:

After pulling in the data sources, I merged all of the data into a single dataset. Next, I checked for the total number of mice and potential duplicates. After confirming duplciates, I sropped the duplciates and pulled all of the non-duplicate data into a seperate dataframe.

To calculate summary statisitics, I used groupby and calculated the mean, median, variance, standard deviation and SEM value.

After retrieiving summary statisitics, I used groupby to create a list of data that outlined the total number of timepoints for all mice tested under each drug regimen. After completing this, I used both pandas and pyplot to create bar charts representing the drug regimens vs. the number of mice tested. The bar charts concluded that Capomulin and Ramicane drug regimens had the highest total testing timepoints. The same process was followed to compare the gender of mice tested, concluding that 51% of the mice tested were male and 49% were female.

To get the quartiles and outliers of the drug regimen data, I used groupby to get the grestest timepoint for each mouse. Then, I merged this data with the original mouse test data to get the tumor volume at the last timepoint. I pu the treatments into a list for looping, and looped through the data to calacuate the IQR and determine if there were any possible outliers. The data showed that there were no outliers for three of the four drugs (Capomulin, Ramicane, or Ceftamin). Infubinol was the only drug with an outlier. Next, I generated a boxplot of the final tumor volume across the four drug regimens. Teh boxplot indicated a lower tumor volume with the Capomulin and Ramicane drugs.

I generated a line plot of the tumor volume and time point for a sample mouse treated with Capomulin. After getting a sample data point, I plotted the data which showed an overall decrease in tumor volume over a 40+ day timeframe of treatment. Thsi insight further inidcated that the Capomulin treament was effective.I also generated a scatterplot of the average tumor volume vs. mouse weight for the Capomulin regimen. It appeared that as the weight (g) increased, tumor volume increased as well. 

The final component to complete the analysis was compute the correlation and linear regression. I used Pearson's to calcuate the correlation, which was 0.84 - indicating very strong correaltion. I added the linear regression to the scatter plot to complete the analysis. 

Overall, the Capomulin regimen and Ramicane had the most data to support its effectiveness and showed lower tumor volume in the mice test subjects compared to other drug regimens. We can conlcude that based on the analysis the Capomulin regimen is more effective in mice at lower weights.












