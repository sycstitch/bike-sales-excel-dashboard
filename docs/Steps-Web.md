# Step-by-Step (Web Version)

# CLEAN UP
## A. Remove duplicates
1. Select all cells.

2. Data tab -> Remove Duplicates.
![alt text](/docs/assets/A-2.png)

3. Ensure 'Select All' and 'My data has headers' is selected, then click 'OK'.
![alt text](/docs/assets/A-3-1.png)
![alt text](/docs/assets/A-3-2.png)

## B. Clarify columns
1. Select entire column, excluding the header. Ctrl-H to pull up "Find and Replace". 

2. Ensure settings match below. Continue for any other columns.
![alt text](/docs/assets/B-2.png)

## C. Convert all numeric values to 'Number' format.
- Not always necessary, but good practice.
1. Select entire column. 

2. Home tab -> Change General to Number
![alt text](/docs/assets/C-2.png)

3. Remove remaining 0s.
![alt text](/docs/assets/C-3.png)

## D. Check for spelling errors or other data entry mistakes.
1. Home tab -> Sort and Filter -> Filter.
- This brings up arrows to see all possible entries in each column.
![alt text](/docs/assets/D-1.png)

2. Press the arrow for each column to check each entry.
![alt text](/docs/assets/D-2.png)

## E. Get rid of 'Miles' in Commute Distance
1. 


## F. Convert Age to age ranges
- Too many individual ages can lead to cluttered visualizations.
![alt text](/docs/assets/F-0.png)

1. Add new column after 'Age'. Name it 'Age Brackets'.

2. Click first cell in column, excluding the header. Add code below.
```
=IF(L2>54,"Old", IF(L2>30,"Middle Age", IF(L2<=30,"Adolescent","Invalid")))
```
- Explanation: 

3. Double click the fill handle (the small square at the bottom-right corner of a selected cell) to auto-fill the rest of the column.
![alt text](/docs/assets/F-3.png)

# PIVOT TABLES & VISUALIZATIONS
- How visualizations are created

1. Create new sheet called 'Pivot Table'.

2. Select a cell. Go to Insert -> Pivot Table.

3. Go to 'bike_buyers'. Ctrl-A to select entire table. Click OK.
![alt text](/docs/assets/PT-setup-3.png)

Should look something like this.
![alt text](/docs/assets/PT-setup-3-2.png)

## 1 - AVG Income
### PIVOT TABLE
1. Select Gender + Income

2. PivotTable Fields -> Values -> Value Field Settings. Click 'Average'.
![alt text](/docs/assets/PT-avg-income-1.png)
![alt text](/docs/assets/PT-avg-income-2.png)

3. Drag 'Purchased Bike' to Columns section.

Finished Product:
![alt text](/docs/assets/PT-avg-income-3.png) 

### VISUALIZATION
1. Click a row in the table. Insert Tab -> Bar graph (clustered column).
![alt text](/docs/assets/Visual-avg-income-1.png)

2. Double click to bring up 'Chart' bar.

3. Turn on 'Axis Title' in both Horizontal and Vertical Axis.
- Horizontal Axis Title: Gender
- Vertical Axis Title: Income
![alt text](/docs/assets/Visual-avg-income-2.png)

4. Set Chart Title.
- Avg Income Per Gender & Salary

5. Add commas to table (looks nicer).
- Select all rows with numbers.
- Home Tab: Change from Number -> Accounting.
- Decrease decimal places to 0.
- Click off table to apply results to graph.
![alt text](/docs/assets/Visual-avg-income-3.png)

## 2 - Commute Distance
![alt text](/docs/assets/Visual-commute-1.png)
- Problem: formatting of '10+' miles doesn't match the others -> can't list distances in order
- Temporary Fix: 
 - Go to original sheet. Rename all instances of "10+ Miles" to "More Than 10 Miles". 
 - Data Tab -> Refresh All

![alt text](/docs/assets/Visual-commute-2.png)
- Chart Type: Line with markers

## 3 - Age Bracket
![alt text](/docs/assets/Visual-age-1.png)

![alt text](/docs/assets/Visual-age-2.png)
- Chart Type: Line with markers

# DASHBOARD
