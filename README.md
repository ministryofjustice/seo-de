# SEO Data Engineering - Technical Test

### Task Introduction
You are the Senior Data Engineer working on a pilot programme to improve the analytical data available to police forces. Your task is to create a dataset to enable analysts to explore the relationship between police 'stop and search' events and the number of police officers on patrol.

Derbyshire police force have supplied some sample patrol data and you need to combine this with their public stop and search data.

We expect this pilot to expand to include more police forces and various time frames. Your code should be written so it can be easily extended and re-used.

You have 4 tasks to complete over the next 45 minutes. You are free to write and structure your code as you see fit. You will be required to present your solution, describe what you have done, how you have done it and why you made each choice.


### 1. Ingest the public 'stop and search' data
This can be found here: https://data.police.uk/docs/ under 'Stop and searches by force'.
We require the data for April 2024, May 2024 and June 2024 for the 'Derbyshire' police force.
The code for the Derbyshire police force is 'derbyshire'.

If you are unable to load this data for any reason, you can find a copy in `raw_data` as `04_stop_and_search.json`, `05_stop_and_search.json` and `06_stop_and_search.json`. Please retain any code you have written.


### 2. Load the patrol data
This is a static csv file stored in the repo at this location: `raw_data/derbyshire_patrol_data.csv`.


### 3. Clean and filter the data.
The 'stop and search' data should be filtered to only include records which:
- have a populated 'age_range' value
- resulted in an arrest (the code for an arrest is `bu-arrest`)

The patrol data must:
- Exclude any days with missing data


### 4. Create an output for the analysts
Combine the data to generate a dataset that provides the total number of 'stop and searches' and patrols occurring each day.
You will need to format the dates in both datasets in order to successfully join them together.

The analysts require a dataset containing the following data:
- The date (formatted as yyyy-mm-dd)
- The total number of patrols occuring that day
- The total number of 'stop and searches' occuring that day

Write out this data set to a new `output_data` folder in a format that can be ingested into a database.
