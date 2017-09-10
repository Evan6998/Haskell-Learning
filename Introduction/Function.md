## Function
函数的声明与它的调用形式大体相同，都是先函数名，后跟由空格分隔的参数表。但在声明中一定要在 = 后面定义函数的行为。  
* Single parameter
```hs
add x = x + 1
```
* Multi parameter
```hs
add x y = x + y
```
* `if` statement
```hs
doubleSmallNumber' x = (if x > 100 then x else x*2) + 1 
```
