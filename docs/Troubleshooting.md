Problem: Pivot Table shows '###' in some cells.
Solutions:
- Refresh data.
- Make cells longer. (It happens because there's not enough space to display numbers.)
  - Select column, right click, 'Column width'
  - 'Autofit' first, then 'Custom' if it reverts again.


Problem: 
"The PivotTable field name is not valid. To create a PivotTable report, you must use data that is organized as a list with labeled columns. If you are changing the name of a PivotTable field, you must type a new name for the field."

Solution: Only select the columns with headers.
- [Source](https://stackoverflow.com/questions/63523302/the-pivottable-field-name-is-not-valid-to-create-a-pivottable-report-you-must)
- Shortcuts to save your headache:
  - Click first header, then Shift + Click the last header.
  - Shift + Cmd/Ctrl + down arrow (selects entire columns)