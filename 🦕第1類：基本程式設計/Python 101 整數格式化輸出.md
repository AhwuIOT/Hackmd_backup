---
comments: true
---
#Python #String #TQC 
#### 題目說明：

請撰寫一程式，輸入四個整數，然後將這四個整數以欄寬為5、欄與欄間隔一個空白字元，再以每列印兩個的方式，先列印向右靠齊，再列印向左靠齊，左右皆以直線 |（Vertical bar）作為邊界。

#### 範例輸入

```
85
4
299
478
```

#### 範例輸出

```

|   85     4|
|  299   478|
|85    4    |
|299   478  |
```

!!! Warning "題目解析"
	這個題目主要是考察你對於格式化輸出的理解以及對於字串處理的能力。具體來說，你需要完成以下任務：

	1. 接收四個整數作為輸入。
	2. 將這四個整數按照特定的格式排列輸出。
	3. 輸出格式要求為：四個整數以欄寬為5、欄與欄間隔一個空白字元，並以每列印兩個的方式，先列印向右靠齊，再列印向左靠齊，左右皆以直線 |（Vertical bar）作為邊界。
	因此，這個題目涉及到對於格式化輸出的處理，以及對於字串格式的理解和操作。
---

#### Solution

```python linenums="1"
a = eval(input())
b = eval(input())
c = eval(input())
d = eval(input())
print("|{:>5d} {:>5d}|".format(a, b))
print("|{:>5d} {:>5d}|".format(c, d))
print("|{:<5d} {:<5d}|".format(a, b))
print("|{:<5d} {:<5d}|".format(c, d))

```

!!! Attention
	=== "format用法"
		`format()` 方法是 Python 中用來格式化字串的一種常用方法，它可以將不同類型的數據插入到字串中的指定位置。以下是 `format()` 方法的基本使用方式：

		```python
		formatted_string = "文字 {} 文字 {}".format(value1, value2)
		```

		這裡的大括號 `{}` 表示將要被替換的位置，而 `value1` 和 `value2` 則是要插入到字串中的值。在這個方法中，可以使用大括號中的數字來指定插入的位置，如 `{0}`、`{1}` 等，這對於同一個值需要多次插入時很有用。

		例如：

		```python
		name = "小明"
		age = 20
		message = "我是{}，今年{}歲。".format(name, age)
		print(message)
		```

		這樣的程式碼會輸出：`我是小明，今年20歲。`

		另外，`format()` 方法還可以用來指定格式，如對齊方式、欄寬等。例如：

		```python
		num = 123
		formatted_num = "{:5d}".format(num)
		print(formatted_num)
		```

		這樣的程式碼會將數字 123 格式化為寬度為 5 的整數，並且向右靠齊輸出，輸出結果為：`  123`。
	=== "input的用法"
		`input()` 函數是 Python 中用來接收用戶輸入的內容的方法。當調用 `input()` 函數時，程式將會暫停執行，等待用戶輸入一些內容，並按下 Enter 鍵。

		```python
		user_input = input("請輸入您的名字：")
		print("您輸入的名字是：" + user_input)
		```

		在這個例子中，當執行到 `input()` 函數時，程式將暫停執行，等待用戶輸入名字。當用戶輸入完名字後，按下 Enter 鍵，`input()` 函數將返回用戶輸入的內容，並賦值給 `user_input` 變量。之後，程式繼續執行，並將用戶輸入的名字打印出來。

		需要注意的是，`input()` 函數返回的內容一般都是字串（`str`）類型，即使用戶輸入的是數字，也會被轉換為字串類型。如果需要使用數字類型，還需要進行類型轉換。

		```python
		user_input = input("請輸入一個數字：")
		number = int(user_input)
		print("您輸入的數字是：" + str(number))
		```

		這樣的程式碼可以讓用戶輸入一個數字，並將其轉換為整數類型，然後打印出來。



!!! Reference
	- [TQC+ 程式語言Python 101 整數格式化輸出](https://jbprogramnotes.com/2020/05/tqc-%e7%a8%8b%e5%bc%8f%e8%aa%9e%e8%a8%80python-101-%e6%95%b4%e6%95%b8%e6%a0%bc%e5%bc%8f%e5%8c%96%e8%bc%b8%e5%87%ba/)
