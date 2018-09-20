# POSTGRESQL - CSV Dialect / Format

Note: See POSTGRESQL TEXT for an alternative CSV Dialect / Format using /t as as separator.


- sep         = ,
- quote       = ?
- escape      = ?
- doublequote = ?
- blanks (ignore empty lines) = false
- trim (leading and trailing spaces) = false


From the PostgreSQL docu:

> This format option is used for importing and exporting the Comma Separated Value (CSV) file format used by many other programs, 
> such as spreadsheets. Instead of the escaping rules used by PostgreSQL's standard text format, 
> it produces and recognizes the common CSV escaping mechanism.
>
> The values in each record are separated by the DELIMITER character. 
> If the value contains the delimiter character, the QUOTE character, the NULL string, a carriage return, or line feed character, 
> then the whole value is prefixed and suffixed by the QUOTE character, 
> and any occurrence within the value of a QUOTE character or the ESCAPE character is preceded by the escape character.
> You can also use FORCE_QUOTE to force quotes when outputting non-NULL values in specific columns.
>
> The CSV format has no standard way to distinguish a NULL value from an empty string.
> PostgreSQL's COPY handles this by quoting. 
> A NULL is output as the NULL parameter string and is not quoted,
> while a non-NULL value matching the NULL parameter string is quoted. 
> For example, with the default settings, a NULL is written as an unquoted empty string, 
> while an empty string data value is written with double quotes ("").
> Reading values follows similar rules. You can use FORCE_NOT_NULL to prevent NULL input comparisons for specific columns.
>
> Because backslash is not a special character in the CSV format, \., 
> the end-of-data marker, could also appear as a data value. To avoid any misinterpretation,
> a \. data value appearing as a lone entry on a line is automatically quoted on output, 
> and on input, if quoted, is not interpreted as the end-of-data marker. 
> If you are loading a file created by another application that has a single unquoted column
> and might have a value of \., you might need to quote that value in the input file.





