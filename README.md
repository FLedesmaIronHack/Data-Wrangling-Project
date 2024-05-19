# data-wrangling-project
Deliverables for week three's data wrangling project.
-------------------------------------------------------------------------
Title of the project: Data-Related Job Salaries
By: Ricardo Torres and Franklin Ledesma
-------------------------------------------------------------------------
Introduction to your project:
    In this project, we conducted an in-depth analysis of data-related salaries using two datasets spanning the years 2020 to 2024. The datasets consisted of a variety of job titles, company locations and salaries with a specific focus on companies based in the United States. Our primary objective was to understand the salary trends within the data industry over this period and to identify key patterns influencing salary variations.
-------------------------------------------------------------------------
Datasets Used:
    We utilized two datasets from Trello: "Data Jobs Salaries - Weekly Updated" and "Data Engineering Jobs in the USA Glassdoor." These datasets were highly similar and contained several overlapping columns, making them ideal for our project. One dataset comprised 18,396 records, while the other contained 1,555 records. Despite the significant difference in the number of records, we conducted our analysis to ensure that the results were representative of the population.
-------------------------------------------------------------------------
Challenges Faced:
    Data Quality and Availability: 
        One of the primary challenges was the quality and availability of datasets. Finding datasets that were both comprehensive and relevant was difficult, as many lacked key columns or had insufficient data to answer our research questions effectively.

    Time Constraints: 
        Time management was another challenge. We started the project later than planned, which led to a rushed timeline towards the end. This limited our ability to refine our visualizations and perform more detailed analysis.

    Data Integration: 
        Merging the two datasets and dealing with duplicate columns required careful handling to ensure data consistency and accuracy.

Strengths:

    Teamwork: 
        Our partnership was marked by excellent communication and simultaneous collaboration. While one of us focused on data cleaning in SQL, the other translated the processes into Python code. This collaborative approach enabled us to learn from each other and enhance our technical skills.

    Complementary Skills: 
        Our complementary skills in SQL and Python helped us efficiently manage different aspects of the data analysis process.

Weaknesses:

    Time Management: 
        Our late start impacted our ability to manage time effectively, leading to a rushed completion of the project. This affected our ability to polish visualizations and conduct more thorough analysis.

Comments:
    Despite these challenges, our combined efforts resulted in a comprehensive analysis of data-related salaries, providing valuable insights into salary trends and high-paying roles within the data industry.

Questions you wanted to answer:
    In this project, we aimed to answer several key questions regarding data-related job salaries using two datasets. 

    Questions:
        1. Are data-related job salaries increasing or declining?
        2. Which is the data-related position with the best pay?
        3. Which state has the best salaries?
        4. Is there a significant difference between remote jobs and non-remote jobs?
        5. Which experience level has the best salary?   
-------------------------------------------------------------------------
Methodology
    Our Process:
        Data Cleaning:

            Initial Inspection and Integration:
                Although the datasets were relatively clean, we needed to integrate and modify certain elements to make them usable for our project. This involved combining the two datasets and aligning their structures.
            
            Column Removal:
                We removed columns that were not relevant to our analysis to streamline the dataset and focus on the variables that mattered most.
            
            Handling Null Values:
                We used the dropna() function to remove rows with null values, ensuring that our analysis was based on complete and accurate data.

            Salary Conversion:
                One of the datasets presented a unique challenge: the salary column contained a mix of hourly rates, monthly rates, and annual salaries. We created a function to standardize all entries to annual salaries. This involved:
                    - Identifying the unit of each salary entry.
                    - Converting hourly and monthly rates to annual salaries using appropriate multipliers (e.g., hourly rate multiplied by 40 and then 52 for annual conversion).

            Cleaning the 'remote_ratio' Column:
                We applied a lambda function to the 'remote_ratio' column to simplify it:
                    - Assigning '1' for remote positions.
                    - Assigning '0' for non-remote positions.

            Location Data Standardization:
                The location column posed another challenge, as values were formatted inconsistently (e.g., 'San Francisco, CL', 'Miami, FL', 'Houston, TX').
                We extracted the state abbreviations from these strings using a function.
                For values that did not fit the pattern, we identified and processed them separately to ensure accurate state extraction.

            Additional Cleaning Techniques:
                We used various other Pandas functions for further cleaning and transformation:
                    .rename(): To standardize column names across both datasets.
                    .concat(): To merge the two datasets into a single DataFrame.
                    .groupby(): To aggregate data and calculate metrics like average salary and record count.
        
        Data Analysis:

            Grouping and Aggregation:

                We grouped the data by relevant columns such as 'job_title' and 'work_year' to calculate the average salary and count of records.

            Filtering:

                We applied filters to focus on job titles with a significant number of records, ensuring the reliability of our analysis.

            Sorting:
             We sorted the grouped data to identify top positions based on average salary and record count.
        
            Visualization:
            Using libraries such as Matplotlib, we created visualizations to illustrate salary trends, compare job roles, and highlight geographical variations in salaries.
        
This thorough methodology ensured that our data was clean, consistent, and ready for insightful analysis. Each step was crucial in addressing the unique challenges presented by the datasets, ultimately enabling us to draw accurate and meaningful conclusions.
-------------------------------------------------------------------------
Conclusions:
    The data-related job salaries are increasing.
        Our analysis confirmed that data-related job salaries have shown a steady increase from 2020 to 2024, reflecting the growing demand for data professionals in the industry.

    AI-related jobs are the best paid data-related jobs in the industry.
        Contrary to our initial hypothesis, AI-related jobs were found to be the best paid data-related roles in the industry, surpassing traditional Data Science positions.

    California is the state with the best salaries.
        The analysis revealed that California, not New York, offers the best salaries for data-related jobs, likely due to the concentration of tech companies in the region.

    There’s no significant difference between remote jobs and non-remote jobs.
        Our findings indicated no significant difference in salaries between remote and non-remote jobs, suggesting that location flexibility does not impact salary levels in the data industry.

    The experience level with the best average salary is the Executive Level.
        Our analysis showed that the Executive Level, not the Senior Level, commands the highest average salary in the data-related job market, reflecting the premium placed on executive experience and leadership skills.
-------------------------------------------------------------------------
Further questions:
    After arriving at the conclusions of our analysis, several further questions could emerge, each flirting for deeper investigation and understanding. Here are some potential questions:

        What factors contribute to the salary increases in data-related jobs?
            Are the increases driven by demand in certain industries, technological advancements, or educational requirements?
            How do economic conditions and market trends influence these salary changes?

        Why do AI-related jobs command higher salaries than traditional Data Science roles?
            What specific skills or qualifications are most valued in AI-related positions?
            Are there particular industries or sectors where AI expertise is especially in demand?

        What makes California the state with the highest salaries for data-related jobs?
            How do cost of living and quality of life factors compare between California and other states?
            Are there specific cities within California that drive this trend, and what industries are most prevalent there?

        What is the distribution of remote vs. non-remote job opportunities in different states and industries?
            Are certain states or industries more inclined to offer remote work options?
            How do remote job opportunities correlate with company size, revenue, or technological infrastructure?

        What differentiates Executive Level roles from Senior Level roles in terms of responsibilities and salary?
            How do job responsibilities, decision-making authority, and leadership roles differ between these levels?
            What career paths and experiences lead to achieving an Executive Level position?

        How does the educational background and experience of individuals in top-paying roles compare across different job titles?
            Are there specific degrees or certifications that are more prevalent among high earners?
            How does the length and type of experience impact salary levels in different data-related roles?

        How do gender, ethnicity, and other demographic factors influence salary trends in data-related jobs?
            Are there noticeable salary disparities based on demographic factors?
            What initiatives or policies can help promote salary equity in the industry?

        What are the future salary projections for data-related jobs based on current trends?
            How might emerging technologies and changing market demands impact future salaries?
            What skills and roles are likely to be most valuable in the next 5-10 years?

        How do bonuses, stock options, and other forms of compensation impact overall earnings in data-related jobs?
            How significant are these additional forms of compensation compared to base salaries?
            Are there trends in how companies offer these benefits based on job titles, experience levels, or locations?

        What is the impact of company size and industry sector on data-related job salaries?
            How do salaries vary between startups, mid-sized companies, and large corporations?
            Which industry sectors offer the most competitive compensation for data professionals?

Exploring these questions would provide a more comprehensive understanding of the factors influencing salaries in the data industry and could inform career strategies for individuals and hiring practices for companies.

Links to data sources and Trello:
    - https://www.kaggle.com/datasets/hamzaelbelghiti/data-engineering-jobs-in-the-usa-glassdoor
    - https://www.kaggle.com/datasets/lorenzovzquez/data-jobs-salaries