Analyzing different covid policies in Power BI

# Project Overview 
The project revolved around the management and analysis of COVID-19 data comprising 10 distinct countries along with the policies implemented to control the spread of the disease. The ultimate goal we were tasked with was to cultivate a hypothesis and subsequently analyze the policy data to find the 3 best policies that would help limit the spread of COVID-19. 
# Management and Data Flow 
The policy datasets utilized in this study were pulled from a myriad of public health departments—World Health Organization, Centers for Disease and Prevention Control (CDC) among others. The data itself was managed using Microsoft Azure services where the policy datasets came from 3 different data sources—Azure SQL Server, CosmosDB and VM SQL Server. Due to the varying file formats, we converted all our data into the parquet file format; parquet was chosen as the appropriate file format due to its optimization in cloud-based storage space coupled with query performance. These parquet files were then brought together under the Azure Data Lake Storage, so all the data could be in one place. After this we transported the data into Azure’s Synapse Analytics so we could load the data onto PowerBI for analysis. 
# Study Design & Methodology 
Assumption: All policies are independent of each other and we focused on policies labeled from c1-8 to rank the top 3 policies among them. 
Variable Measure: The proportion of cases with respect to the population of the country that occurred while a policy was present. Countries’ population data came from Google and were representative of 2020. 
# The steps of the Analysis Plan are as follows: 
1. We expected the best policies to have relatively low COVID cases compared to other policies.. In order to calculate proportion, we imported a new table with population information. Then We created a table for each policy. The table had the date, sum of confirmed, country name, flag of the policy, the level of the policy, and the population. We made a new column and calculated proportions as well.
2. Using these tables, we made graphs for each policy. X-axis represents the average proportion, and the y-axis represents the countries (divided again by 0 and 1 depending on the flag). We also made graphs to display counts of 0’s and 1’s for each country, separated per policy. 
3. After exporting tables we made for policies, we calculated the weighted average of the proportion and imported them back into the Power BI.  These tables are labeled stat1-8.  
4. Using the stat tables, we made our final graph displaying the ranks of the policies. The policies followed the same pattern for all countries. We picked three policies with the lowest proportions.
# Results 
All policies followed a somewhat similar pattern for all countries. We picked the policies with the least number of weighted average proportions of cases and decided they are the best policies. They are policy 8, policy 4, and policy 3. 
# Conclusion
The best 3 policies according to our outlined analysis are International travel control, Restrictions on public gatherings, and the Cancellation of public events. 
