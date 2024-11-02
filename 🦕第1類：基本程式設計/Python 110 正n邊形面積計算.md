---
comments: true
---
#Python #TQC 
#### 題目說明：

請撰寫一程式，讓使用者輸入兩個正數n、s，代表正n邊形之邊長為s，計算並輸出此正n邊形之面積（Area）。

!!! Tip
	提示1：建議使用import math模組的math.pi及math.tan  
	提示2：正n邊形面積的公式如下：
	$Area=(n∗s^2)/(4∗tan(pi/n))$
	提示3：輸出浮點數到小數點後第四位

#### 範例輸入

```
8
6
```

#### 範例輸出

```
Area = 173.8234
```

!!! Warning "題目解析"
	1. 首先，使用者被要求輸入兩個正數，分別代表正n邊形的邊數n和邊長s。
	2. 然後，程式將這兩個數字分別儲存在變數 `n` 和 `s` 中。
	3. 接下來，程式根據給定的公式計算正n邊形的面積。這個公式利用了正n邊形的邊數和邊長，以及 `math` 模組中的 `math.tan()` 函數和 `math.pi` 常數。
	4. 最後，程式將計算得到的面積值格式化輸出，要求輸出到小數點後第四位。

	根據這個解答，我們可以得出以下結論：

	- 解決這個問題的關鍵在於理解正n邊形面積的計算公式，以及如何在程式中利用這個公式。
	- 程式碼使用了 `math` 模組中的 `math.tan()` 函數和 `math.pi` 常數，這樣可以更方便地進行數學運算。
	- 最後，程式將計算結果格式化後輸出給使用者。

---

#### Solution

```python linenums="1"
import math
n = eval(input())
s = eval(input())
a = (n*(s**2)) / (4*math.tan(math.pi/n))
print("Area = %.4f"%a)

```

!!! Reference
	- [TQC+ 程式語言Python 110 正n邊形面積計算 - JB 程式筆記 (jbprogramnotes.com)](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-110-%e6%ad%a3n%e9%82%8a%e5%bd%a2%e9%9d%a2%e7%a9%8d%e8%a8%88%e7%ae%97/)