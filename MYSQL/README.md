# MYSQL - CSV Dialect / Format

- sep         = \t
- quote       = nil
- escape      = \\
- doublequote = false



By default MYSQL exports to:

> If you specify no FIELDS or LINES clause, the defaults are the same as if you had written this:
>
>     FIELDS TERMINATED BY '\t' ENCLOSED BY '' ESCAPED BY '\\'
>      LINES TERMINATED BY '\n' STARTING BY ''
>
> (Backslash is the MySQL escape character within strings in SQL statements, 
> so to specify a literal backslash, you must specify two backslashes for the value to be interpreted as a single backslash. 
> The escape sequences '\t' and '\n' specify tab and newline characters, respectively.)




Edges Cases:

- how to handle newlines in values - use \n?
- how to handle tabs in values - use \t (note: "escpaced" \t is different from the "literal" ascii/char code in a text file?
- how to handle empty lines?
- how to handle empty fields? use "explicit" \N for null
- how to handle leading and trailing spaces in values?

