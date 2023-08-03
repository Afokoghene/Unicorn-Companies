![image](https://github.com/Afokoghene/Unicorn-Companies/assets/114203869/6bea549a-858e-4898-9646-b44f3136278d)# Unicorn Companies
Analysis to gain performance insights from dataset containing information on 1,074 Unicorn Companies.

---

> [Introduction](https://github.com/Afokoghene/Unicorn-Companies/#introduction) <br>
> [Problem Statement](https://github.com/Afokoghene/Unicorn-Companies/#problem-statement) <br>
> [Skills Demonstrated](https://github.com/Afokoghene/Unicorn-Companies/#skills-demonstrated) <br>
> [Data Sourcing](https://github.com/Afokoghene/Unicorn-Companies/#data-sourcing) <br>
> [Data Assessment and Transformation](https://github.com/Afokoghene/Unicorn-Companies/#data-assessment-and-transformation) <br>
> [Data Analysis](https://github.com/Afokoghene/Unicorn-Companies/#data-analysis) <br>
> [Data Visualization](https://github.com/Afokoghene/Unicorn-Companies/#data-visualization) <br>
> [Insights](https://github.com/Afokoghene/Unicorn-Companies/#insights) <br>

---

## Introduction
Becoming a Unicorn for a company can be compared to a country winning the FIFA World Cup, or even better, you coming first in a global competition. All the listed scenarios come with joy, as they signify reaching a significant milestone after putting in hard work and being patient enough. As for Unicorn Companies, they are privately held companies that have a current valuation of $1 billion or more.

This dataset contains 1,074 privately held companies that have reached a valuation of $1 billion. The analysis to be carried out aims to gain insights into how these companies have performed during the recorded period and also to identify the year with the highest number of companies becoming unicorns, among other things. 
I will conduct all the analysis processes on MS Excel as I am trying to improve my Excel skills, and this is part of the process.

---

## Problem Statement
The problem statment are the questiosn that are to be answered from the dataset

1. Which unicorn companies have had the biggest return on investment?
2. How long does it usually take for a company to become a unicorn? Has it always been this way?
3. Which countries have the most unicorns? Are there any cities that appear to be industry hubs?
4. In what year did the most companies become unicorns?
4b. What is the average return on investment for companies that join each year? Are there any significant trends or variations over time?
5. Which industry has the highest average Return On Investment (ROI) percentage?
6. Which continent has the highest number of companies in the dataset, and what are the most common industries among them?

---

## Skills Demonstrated
- Cleaning and transformation of data in MS Excel
- Aggregation and Pivot tables in MS Excel
- Visualization of data in MS Excel

---

## Data Sourcing
The dataset was obtained from [Maven Analytics'](https://www.mavenanalytics.io/data-playground?accessType=open&dataStructure=5wfxyeVf1etbP4TXdyPdG1) website where datasets are generally available for practice purposes.

---

## Data Assessment, Cleaning / Transformation
### Assessment
The dataset was found in a CSV file format and was converted to an Excel workbook to enable editing and save progress.

The dataset originally contained 1,074 rows and 10 columns but during transformation of the dataset, 8 more columns were included to enable easy analysis and agregation.

- The following columns originally came with the dataset
1. Company: The name of the company
2. Valuation: Company valuation in Billions of Dollars but in the format 1B, 2B e.t.c
3. Date Joined: The date in which the company reached $1 billion in valuation
4. Industry: Industry that the company falls under
5. City: City the company was founded in
6. Country: Country the company was founded in
7. Continent: Continent the company was founded in
8. Year Founded: Year the company was founded
9. Funding: Total amount raised across all funding rounds in billions (B) or millions (M) of dollars
10. Select Investors: Top 4 investing firms or individual investors (some have less than 4)

- The following columns were added after transformation:
1. Valuation-C: This column displays the valuation in full figures instead of using $1B or $2B notations.
2. Year Joined: This column indicates the year when each company reached a valuation of $1B. It was derived from the Date Joined column, as the year was necessary for the analysis process.
3. Funding-C: This column shows the total amount raised across all funding rounds in full figures instead of using short forms.
4. Return On Investment (Percent): This column calculates the return on investment for each company based on the Funding and Valuation columns.
5. Diff Between Joined and Founded Year: This column represents the difference between the year each company reached a valuation of $1B and the year they were founded.
6. Select Investor: Four (4) columns were created from this particular column, mainly to hold each investor's information for companies in different cells.

---

### Cleaning / Transformation

1. The dataset was checked for duplicates and none was found.
2. The Substitute function and FlashFill were used to create and fill the Valuation-C column from the Valuation column. This was done to change the format of the column and make it easy for calculations to be done using values from the column.
3. Employed the RIGHT function to get the last 4 digits from the Date Joined to fill the Year Joined column.
4. To obtain the column 'Funding-C,' we first filtered the dataset based on the 'Funding' column to display only rows that ended with 'B' (representing billions). After applying the filtration, we utilized the substitute function twice: once to remove the dollar sign and another time to replace 'B' with '000000000.' This method successfully converted all the rows in billions into the desired format.
5. To acquire the 'Funding-C' column, we initially applied a filter to the dataset, showing only those rows in the 'Funding' column that ended with 'M' (representing millions). Once the filtering was done, we utilized the substitute function twice: the first time to eliminate the dollar sign and the second time to replace 'M' with '000000.' This approach effectively converted all million-based rows into the desired format.
6. This formula **ROI = (Valuation - Funding) / (Valuation) * 100** was used to calculate the Return On Invesment and the result was filled in the 'Return On Investment (Percent)' column.
7. To obtain values for the 'Diff Btw Year Joined and Founded Year' column, simply subtracted the Year Joined from the Year Founded.
8. The Select Investors column had each cell carrying at least 2 investors ' name so I separated each investor to different cells which made us have 4 rows for Select Investors. This was successfully done using the Text To Columns feature on Excel and it was separated based on the comma delimiter.

---

## Data Analysis















