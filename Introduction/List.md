## List
在ghci下，我们可以使用let关键字来定义一个常量。  
**在Haskell中，List是一种单类型的数据结构，可以用来存储多个类型相同的元素。**
```hs
let lostNumbers = [4,8,15,16,23,48]   
```
- ++
```hs
ghci> [1,2,3,4] ++ [9,10,11,12]    
ghci> [1,2,3,4,9,10,11,12]
```
字符串实际上就是一组字符的List   
**`++` will traverse the whole list, so use it cautiously in large list**

- `:` operator   
可以连接一个元素到一个List或者字符串之中，而++运算符则是连接两个List
```hs
'A':" SMALL CAT"   
>> "A SMALL CAT"   
5:[1,2,3,4,5]  
>> [5,1,2,3,4,5] 
```

* !!
```hs
ghci> "Steve Buscemi" !! 6   
'B'   
ghci> [9.4,33.2,96.2,11.2,23.25] !! 1   
33.2 
```

* 大小比较  
当List内装有可比较的元素时，使用 > 和 >=可以比较List的大小。它会先比较第一个元素，若它们的值相等，则比较下一个，以此类推。
```hs
ghci> [3,2,1] > [2,1,0]   
True   
ghci> [3,2,1] > [2,10,100]   
True   
ghci> [3,4,2] > [3,4]   
True   
ghci> [3,4,2] > [2,4]   
True   
ghci> [3,4,2] == [3,4,2]   
True 
```
* 常用函数
1. head **返回收个元素**
2. tail **返回[1:]**
3. last **返回最后一个元素**
4. init **返回[:-1]**  
![listmonster](listmonster.png)
5. length
6. null
7. reverse
8. take **返回前几个元素**
```hs
ghci> take 3 [0,1,2,3,4,5]
[0,1,2]
```
9. maximum
10. sum
11. elem **判断一个元素是否属于某个list, 中缀形式调用**
```hs
ghci> 4 `elem` [3,4,5,6]   
True   
ghci> 10 `elem` [3,4,5,6]   
False 
```
