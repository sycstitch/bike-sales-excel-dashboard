# Step-by-Step (Web Version)

> **Note:** Due to Excel Web limitations (no slicers from charts, no copying pivot tables between sheets), this guide keeps *everything* on a single sheet: the **Dashboard**. Pivot tables will be hidden behind the visuals.

---

## CLEAN UP

### A. Remove duplicates  
1. Select all cells.  
2. **Data tab → Remove Duplicates**  
   ![alt text](/docs/assets/A-2.png)  
3. Make sure **‘Select All’** and **‘My data has headers’** are checked, then click **OK**.  
   ![alt text](/docs/assets/A-3-1.png)  
   ![alt text](/docs/assets/A-3-2.png)

### B. Clarify columns  
1. Select the column (no header), press **Ctrl+H**.  
2. Set up Find & Replace as needed.  
   ![alt text](/docs/assets/B-2.png)

### C. Format numbers  
1. Select the column.  
2. **Home tab → Format → Number**  
   ![alt text](/docs/assets/C-2.png)  
3. Remove any leftover 0s.  
   ![alt text](/docs/assets/C-3.png)

### D. Catch typos  
1. **Home → Sort & Filter → Filter**  
   ![alt text](/docs/assets/D-1.png)  
2. Use filter arrows to review unique values in each column.  
   ![alt text](/docs/assets/D-2.png)

### E. Clean up Commute Distance  
1. **Ctrl+H**  
   - **Find:** ` Miles`  
   - **Replace:** *(leave blank)*  
   - Limit to Commute Distance column.

### F. Bucket Age into ranges  
1. Add a new column after **Age**, name it **Age Brackets**.  
2. Paste into first cell (below header):  
   ```excel
   =IF(L2>54,"Old", IF(L2>30,"Middle Age", IF(L2<=30,"Adolescent","Invalid")))
   ```  
3. Double-click the fill handle.  
   ![alt text](/docs/assets/F-3.png)

---

## DASHBOARD (Pivot Tables + Charts)

1. Create a new sheet called **Dashboard**. This is where *everything* goes.

### 1 - Avg Income by Gender + Purchase Status  
#### Pivot Table  
1. Insert → Pivot Table → Select entire dataset  
2. **Rows:** Gender  
   **Columns:** Purchased Bike  
   **Values:** Income → Set to **Average**  
   ![alt text](/docs/assets/PT-avg-income-1.png)  
   ![alt text](/docs/assets/PT-avg-income-2.png)  
   ![alt text](/docs/assets/PT-avg-income-3.png)

#### Chart  
1. Click table → Insert → **Clustered Column Chart**  
   ![alt text](/docs/assets/Visual-avg-income-1.png)  
2. Enable **Axis Titles**:  
   - Horizontal: Gender  
   - Vertical: Income  
   ![alt text](/docs/assets/Visual-avg-income-2.png)  
3. Title: `Avg Income by Gender & Purchase Status`  
4. Format income numbers:  
   - Select them → Format: **Accounting**, 0 decimals  
   - This also updates the graph  
   ![alt text](/docs/assets/Visual-avg-income-3.png)

### 2 - Commute Distance  
1. Insert Pivot Table:  
   - **Rows:** Commute Distance  
   - **Values:** Count of any field (e.g., ID or Email)  
2. If "10+ Miles" exists, rename to `"More Than 10 Miles"` in the original dataset.  
   ![alt text](/docs/assets/Visual-commute-1.png)  
3. Refresh Pivot Table → Insert **Line Chart with Markers**  
   ![alt text](/docs/assets/Visual-commute-2.png)

### 3 - Age Brackets  
1. Insert Pivot Table:  
   - **Rows:** Age Brackets  
   - **Values:** Count  
2. Insert **Line Chart with Markers**  
   ![alt text](/docs/assets/Visual-age-1.png)  
   ![alt text](/docs/assets/Visual-age-2.png)

---

## LAYOUT AND POLISH

1. **Hide Pivot Tables**  
   - Present in the 'AA' column.

2. **Remove gridlines**  
   - Sheet Background: Ctrl+A → **View tab → Uncheck Gridlines**
   - Graphs: Click on the lines, and under Vertical Axis, uncheck 'Major Gridlines'.

3. **Add Labels to graphs**
  - Double click or right click on an element to add data labels, customize text, and move data labels.

4. **Add Dashboard Title**  
   - Select cells at the top → Fill with color  
   - **Merge & Center** → Type your dashboard name  
   ![alt text](/docs/assets/Dashboard-3.png)  
   ![alt text](/docs/assets/Dashboard-3-2.png)

5. **Arrange visuals**  
   - Manually align charts (multi-select doesn’t work well in Web).  
   - Reference:  
     - [Align or arrange objects](https://support.microsoft.com/en-us/office/align-or-arrange-objects-bfd91078-2078-4b35-8672-f6270690b3b8#id0ebbf=web)  
     - [Customize keyboard shortcuts](https://support.microsoft.com/en-us/office/customize-keyboard-shortcuts-9a92343e-a781-4d5a-92f1-0f32e3ba5b4d)

6. **Slicers (Optional)**  
  - Select a table. Insert Tab -> Slicer.
    - Pick Marital Status, Region, Education.
  - Let slicers affect all graphs.
    - Double click the slicer. 
    - Slicer Settings -> PivotTable connections -> Select all.
      ![alt text](/docs/assets/Dashboard-5.png)
        - Ignore the 'Pivot Table' sheet. I had to start over but I kept the sheet so you'd know what it'd look like if the pivot tables were made on Desktop.

## FINISHED PRODUCT
![alt text](/docs/assets/finished-product.png)