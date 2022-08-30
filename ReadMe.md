## Delete records based on the id provided

This stored procedure helps you to easily delete a record from a table without writing again and again the Delete statement. The only info that have to be provided are schema and table name, followed by the column name and the value you want to delete.<br />
This was used in a banking application.

## Execution syntax 👩‍💻

exec [crc].[DeleteRecordById] @schema= 'your schema name', @table ='your table name', @column_n ='the column name based on which the delete will be done', @value = 'desired value'

## Other info

This stored procedure has integrated binding params part to protect the db against SQL Injection, added trim function & quotename for replacing square brackets and beautifying the code.
<br />
‼ For those who want to run this sp on older versions of SQL Server, replace the trim function with a combination of ltrim and rtrim functions (example: ltrim(rtrim(column_name)) );
If you have permission, update the db compatibility level to 130 and you can forget about the above combination 😉

