# Flow-Utilities

Misc. ServiceNow Workflow Studio flows, subflows, and actions utilities. These are agnostic solutions and meant as enhancements to ServiceNow delevelopment.

## Excel Action Utilities

### Excel Get Sheets 

__About__ Retrieves the list of worksheets within an Excel file. 

__Inputs__
- _Excel file_ is a reference to the sys_attachment table. The file needs to an an .xlsx file.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Sheets_ an array of sheet namess found in the Excel file.
- __Sheet_ a comma separated string of Sheets.
- _Found_ is the number of sheets found.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.

### Excel Get Sheet

__About__ Retrieves information pertaining to the Excel sheet.

__Inputs__
- _Excel file_ is a reference to the sys_attachment table. The file needs to an an .xlsx file.
- _Sheet_ is the Excel sheet to get information about.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Columns_ an array of column names in the Sheet.
- __Columns_ a comma separated string of Columns.
- _Column count_ is the number of columns in the Sheet.
- _Rows_ an array of row names in the Sheet.
- __Rows_ a comma separated string of Rows.
- _Row count_ is the number of rows in the Sheet.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.

### Excel Get Rows

__About__ Retrieves all of the column and row data from an Excel sheet.

__Inputs__
- _Excel file_ is a reference to the sys_attachment table. The file needs to an an .xlsx file.
- _Sheet_ is the Excel sheet to get information about.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Sheet_ a JSON object containing all of the sheet data.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.

### Excel Get Row

__About__ Retrieves all of the column data from an Excel sheet row.

__Inputs__
- _Excel file_ is a reference to the sys_attachment table. The file needs to an an .xlsx file.
- _Sheet_ is the Excel sheet to get information about.
- _Row_ is the row number to retrieve. Note that rows starts with number of 1.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Row_ a JSON object containing all of the row data.
- __Row_ a string represenation of the row data.
- _Found_ 1 found the row; else 0.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.

### Excel Get Cell

__About__ Retrieves specific column and row value from an Excel sheet.

__Inputs__
- _Excel file_ is a reference to the sys_attachment table. The file needs to an an .xlsx file.
- _Sheet_ is the Excel sheet to get information about.
- _Row_ is the row number to retrieve. Note that rows starts with number of 1.
- _Column_ is the column name to retrieve.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Cell_ a string of the data at the row and coilumn.
- _Found_ 1 found the row; else 0.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.
- Excel Find Cells

## JSON Action Utilities

- 
