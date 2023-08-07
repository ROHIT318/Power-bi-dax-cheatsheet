# Power BI DAX Cheatsheet
---
##  Format Strings and Integers
1. `FORMAT(value, "")`: Produces string
```
-532.00 -> -532
0.32 -> 0.32
```
2. `FORMAT(value, "0")`: Produces string
```
-532.00 -> -532
0.32 -> 0
```
3. `FORMAT(value, "0.0" )`: Produces string
```
-532.00 -> -532.0
10.26 -> 10.3
```
<b>NOTE:</b> All upper formula produces a string as final result. Can not be sorted as an integer. To sort as an integer, select measure under "measure tools" section, select `dynamic` in `format` dropdown.<br/>
5. `0.0`: Produces integer
```
-532.00 -> -532
0.32 -> 0.32
```
6. "00.00": Produces integer
```
3.2 -> 03.20
```
7. "#.#": Produces integer
```
-532.00 -> -532
0.32 -> .3
10.00 -> 10
```
<b> Add Commas to integer: </b><br/>
8. "#,K":
```
-532.0 -> -532K
0.32 -> K
1,243.00 -> 1243K
```
9. "#,.K":
```
10.26 -> K
1,243.00 -> 1K
143,498.00 -> 143K
```
10. "0,.#K": Two commas are million, one comma is thousand, 3 = Billion
```
-532.00 -> -0.5K
10.26 -> 0K
1,243.00 -> 1.2K
```
11. "#%":
```
0.32 -> 32%
2.00 -> 200%
1,243.00 -> 124300%
```
12. "$0,#.#":
```
-532 -> -$532
10.26 -> $10.3
1,243 -> $1,243
```
13. "$0,#.#;($0,#.#);zero":
```
-532.00 -> ($532)
10.26 -> ($10.3)
0.00 -> zero
```
## Format Dates:
1. FORMAT(MAX(dateTable[DateColumn), "0"):
```
15 February 2023 -> 44972
```
2. FORMAT(MAX(dateTable[DateColumn), "dd mm yyyy"):
```
15 February 2023 -> 15 02 2023
```
3. FORMAT(MAX(dateTable[DateColumn), "dd/mm/yyyy"): `/` or " " or "-" are just separators. Any can be used.
```
15 February 2023 -> 15/02/2023
```
**NOTE:** "mmm" -> Jan; "m" -> 1 (and not 01), 12; d -> 1 (and not 01),12; ddd -> Thu, Sun; "q" (->1,2,3,4) gives quarter in which the date belongs to, can be combined with date, month, year. "\Qq" -> Q1,Q2,Q3,Q4.





























