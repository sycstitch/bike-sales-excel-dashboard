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

# PIVOT TABLES
