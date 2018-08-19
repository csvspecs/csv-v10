# Comma-Separated Values (CSV) Datafiles for Testing

Quotes in quotes, newlines in quotes, blank lines, comments, crlf,
comma in quotes and more


## Summary


[simple.csv](simple.csv):
```
a,b,c
1,2,3
```
=>
``` json
[["a", "b", "c"],
 ["1", "2", "3"]]
```

[utf8.csv](utf8.csv):
```
a,b,c
1,2,3
4,5,ʤ
```
=>
``` json
[["a", "b", "c"],
 ["1", "2", "3"],
 ["4", "5", "ʤ"]]
```

[empty.csv](empty.csv):

```
a,b,c
1,,
2,3,4
```
or
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


[comma_in_quotes.csv](comma_in_quotes.csv):

```
first,last,address,city,zip
John,Doe,120 any st.,"Anytown, WW",08123
```
=>
``` json
[["first", "last", "address",     "city",        "zip"  ],
 ["John",  "Doe",  "120 any st.", "Anytown, WW", "08123"]]
```

[newlines.csv](newlines.csv):
```
a,b,c
1,2,3
"Once upon↵
a time",5,6
7,8,9
```
=>
``` json
[["a", "b", "c"],
 ["1", "2", "3"],
 ["Once upon\na time", "5", "6"],
 ["7", "8", "9"]]
```


[escaped_quotes.csv](escaped_quotes.csv):
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

[quotes_and_newlines.csv](quotes_and_newlines.csv):
```
a,b
1,"ha↵
""ha""↵
ha"
3,4
```
=>
``` json
[["a", "b"],
 ["1", "ha\n\"ha\"\nha"],
 ["3", "4"]]
```

[json.csv](json.csv):
```
key,val
1,"{""type"": ""Point"", ""coordinates"": [102.0, 0.5]}"
```
=>
``` json
[["key", "val"],
 ["1",   "{\"type\": \"Point\", \"coordinates\": [102.0, 0.5]}"]]
```
