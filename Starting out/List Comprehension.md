## List Comprehension
- 使用haskell语句模拟集合表示形式
<a href="https://www.codecogs.com/eqnedit.php?latex=S&space;=&space;\left&space;\{&space;2*x|x\in\mathbb{N},x&space;\leq&space;10&space;\right&space;\}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?S&space;=&space;\left&space;\{&space;2*x|x\in\mathbb{N},x&space;\leq&space;10&space;\right&space;\}" title="S = \left \{ 2*x|x\in\mathbb{N},x \leq 10 \right \}" /></a>
```hs
ghci> [x*2 | x <- [1..10]]   
[2,4,6,8,10,12,14,16,18,20]
```
- 限制条件
```hs
ghci> [x*2 | x <- [1..10], x*2 >= 12]   
[12,14,16,18,20] 
```
```hs
ghci> [ x | x <- [50..100], x `mod` 7 == 3]   
[52,59,66,73,80,87,94]
```
```hs
boomBangs xs = [ if x < 10 then "BOOM!" else "BANG!" | x <- xs, odd x]  
ghci> boomBangs [7..13]   
["BOOM!","BOOM!","BANG!","BANG!"] 
```  
`boomBangs`是一个**函数**
