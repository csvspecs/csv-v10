# Comma-Separated Values (CSV) Datafiles for Testing

Quotes in quotes, newlines in quotes, blank lines, comments, crlf,
comma in quotes and more



## Summary

comma_in_quotes.csv:

```
first,last,address,city,zip
John,Doe,120 any st.,"Anytown, WW",08123
```
=>
``` json
[["first", "last", "address",     "city",        "zip"  ],
 ["John",  "Doe",  "120 any st.", "Anytown, WW", "08123"]]
```

empty:

```
a,b,c
1,"",""
2,3,4
```
=>
``` json
[["a", "b", "c"],
 ["1", "",  "" ],
 ["2", "3", "4"]]
```

escaped_quotes:
```
a,b
1,"ha ""ha"" ha"
3,4
```
=>
``` json
[["a", "b"],
 ["1", "ha \"ha\" ha"],
 ["3", "4"]]
```
