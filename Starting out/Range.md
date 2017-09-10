## Range
Range是构造List方法之一，而其中的值必须是可枚举的，像1、2、3、4...字符同样也可以枚举，字母表就是A..Z所有字符的枚举。
```hs
ghci> [1..20]   
[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20]   
ghci> ['a'..'z']   
"abcdefghijklmnopqrstuvwxyz"   
ghci> ['K'..'Z']   
"KLMNOPQRSTUVWXYZ"
```
- 步长
前两个**数字/字母**的差作为间距，再枚举所有的元素
```hs
ghci> [2,4..20]   
[2,4,6,8,10,12,14,16,18,20]   
ghci> [3,6..20]   
[3,6,9,12,15,18]  
```
取24个13的倍数
```hs
take 24 [13,26..]
```
由于haskell是**惰性**的，它不会对无限长度的List求值  

- cycle
```hs
ghci> take 10 (cycle [1,2,3])   
[1,2,3,1,2,3,1,2,3,1]   
ghci> take 12 (cycle "LOL ")   
"LOL LOL LOL "  
```
- repeat
```hs
ghci> take 10 (repeat 5)   
[5,5,5,5,5,5,5,5,5,5] 
```

