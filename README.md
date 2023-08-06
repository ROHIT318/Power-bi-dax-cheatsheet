# Power BI DAX Cheatsheet
---
##  Format strings
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
<b>NOTE:</b> All upper formula produces a string as final result. Can not be sorted as an integer. To sort as an integer, select measure under "measure tools" section, select `dynamic` in `format` dropdown.
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












