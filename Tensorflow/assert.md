## Assert - Assertion 斷言
- 程式執行到某時間, 斷定必然狀況的狀態, 斷言該時間點時, 某變數必定是某值或某種特性     
斷言執行前後不可以改變任何code, compile 不會包含 asssert
```
	assert <test>, <message>
```
- test
狀態測試
- message
斷言失敗後要呈現的message, Ex: 提款機負值

- Code Example
```
	class Account:
		def __init__(self, number, name):
			self.number = number
			self.name =name
			self.balance = 0

		def deposit(self, amount):
			assert amount > 0,
			self.balance += amount

		def withdraw(self, amount):
			# amount 一定要是正數, 不會是負數
			assert amount > 0, 
			if amount <= self.balance:
				self.balance -= amount
			else:
				raise RuntimeError('balance is not enough')

	a = Acount('E122', 'Quert')
	a.deposit(-1)
```

```
	class Stack:
		def __init__(self):
			self.idx = 0
			self.data = []

		def push(self, c):
			length = len(self.data)
			self.data.append(c)
			assert (length - 1) == len(self.data)
			return ele
```
