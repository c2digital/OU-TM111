---
title: TM111 - Part 4 - TMA practice
created: '2024-09-15T18:39:16.549Z'
modified: '2024-09-15T18:39:52.950Z'
---

# TM111 - Part 4 - TMA practice

## Requirements:-
•	200 words
•	Number of search queries processed
•	Type of searched used by the project to make predictions
•	Discuss level of success
•	Discuss concerns over privacy of google users

## Research Notes:-
•	25 countries
•	Aggregated search queries
•	Launched in 2008 until 2015. Current data are offered for research only.
•	Monitoring users health tracking behaviours, queries can be analysed to reveal present of flu-link illness in a population
•	Compared findings to historic baseline levels for each region
•	Returned level as minimal, low, moderate, high or intense.
•	Estimated level had been generally consistent with health agency data
•	Method involved using a time series covering 50 million common queries entered in a week within the US.
•	The queries time series is computed separately for each state.
•	The users IP address for the search was used to identify which state the query originated
•	A linear model was used to determine the top 45 queries which, when compared to CDC data, most accurately resulted in the user visiting a doctor. The trained model was then used to predict flu outbreak across the US.
•	Avoids privacy violations by aggregating millions of anonymous search queries without identified the individual user. 
•	The search log contains the IP address which could be used to trace to the region the query was submitted from. Google implemented a policy to anonymous IP addresses after 9 months.
•	Process is automated, no human involvement.
•	Electronic Privacy Information Center and Patient Privacy Rights have voiced concerns that whilst the data could support public health in significant ways, the had worries that user-specific investigations could be compelled by courts.
•	CDC reported GFT could predict regional outbreaks up to 10 days before they received reports. In 2009 GFT noticed a regional pandemic 2 weeks before the CDC released a report.
•	Roughly 36,000 US citizens die each year from the flu.
•	A paper from Google stated predictions were 97% accurate when compared to CDC data
•	GFT failed to predict the 2009 spring pandemic
•	Consistently overestimated flu incident during 2011-2013. Predicted twice as many doctor visits during the 2012 flu season.
•	A 2022 study noted GFT is outperformed by ‘recency heuristic’ which uses naïve forecasting. GFT had an error ate of 0.38 compared to recency heuristic’s 0.20.
•	People making flu related searches know little about how to diagnose flu and may just be researching symptoms that are similar to flu.
•	Analysis of terms including ‘fever’ and ‘cough’ along with changes in the search algorithm over time have raised concerns about the predictions.
•	Google had to compensate for increases in searches due to the prominence of flu in the news in 2013 which had been found to skew results.
•	A later study however concluded that combining GFT data with CDC data could improve estimates and reduce errors when compared to just using the CDC data (by over 50%)
•	An assessment of the GFT model found the model was also aggregating queries about different health conditions resulting in an overprediction of doctor visits.
•	Follow up work has been able to substantially improve the accuracy through the use of techniques such as random forest regression models.

## Answer (205 words)
Google Flu Trends (GFT) is a project that predicts the spread of flu at a regional and national level. It tracks 45 selected queries along with IP addresses to determine regions where more people were searching for flu related symptoms, indicating  increased flu in that area.

Early reports indicated a 97% accuracy when compared to Center for Disease Control (CDC) data. During a pandemic in 2009 GFT noted the increase nearly two weeks before the CDC. Later reports found the solution to be outperformed by newer techniques such as ‘recency heuristics’.

GFT also had some failures including failing to spot the 2009 spring pandemic and overestimating the 2013 season due to increased searches following flu related news stories.

Privacy concerns were raised by several organisations which, while noting the public heath benefits, were also concerned about how user-specific data could be used by entities including courts as a search could be tracked back to the user via the IP address.

GFTs privacy protections included the running without human intervention and anonymising IP addresses in its logs after 9 months.
Whilst GFT wasn’t always spot on, several studies have found the project to produce beneficial data – especially when used alongside other datasets such as the CDCs.

