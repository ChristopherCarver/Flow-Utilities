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

## JSON Action Utilities

### JSON Set Value

__About__ Inserts or updates a key value in a JSON structure.

__Inputs__
- _JSON_ the JSON object.
- _Path_ a a period delimited string that provides the path where to add the key and value.
- _Key_ is the string key to insert or update.
- _Value_ is the string value of the key.
- _Value type_ re-casts the value to the proper JSON datatype. 
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _JSON_ the new JSON object with the added key and value.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.

### JSON Get Values

__About__ Retrieves all of the JSON structure values that match the key.

__Inputs__
- _JSON_ the JSON object.
- _Key_ to search for.
- _Regex_ is a toggle stating that they Key provided is a regex pattern.
- _Regex flags_ see https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp 
- _Depth_ is JSON structure depth to traverse. Default is 0 meaning traverse the entire structure.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Values_ as an array of strings holding all of the values found.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.


### JSON Get Value

__About__ Retrieve specific JSON value that match the key.

__Inputs__
- _JSON_ the JSON object.
- _Key path_ is a period delimited string to the key within the JSON object to retrieve the value.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Value_ the string represenation of the value.
- _Value type_ the typeof the value; note that object is changed to either array or json to distinguish both.
- _Found_ is true if the value was found; else, false.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.

### JSON Get Keys

__About__ Retrieves all of the JSON structure keys.

__Inputs__
- _JSON_ the JSON object.
- _Depth_ is JSON structure depth to traverse. Default is 0 meaning traverse the entire structure.
- _Log_ is a toggle to add a log entry of the resulting outputs.

__Outputs__
- _Keys_ as an array of strings holding all of the keys found.
- _Key paths_ as an array of strings holding all of period delimited key strings found.
- _Error_ is true if an error was encoutered; else false.
- _Error message_ contains the error message if an error was encountered.
