# Assignment 1: Basic

<br>

##### 1. Define a variable <code class="highlighter">pi</code> and assign a value to it.

```swift
let pi: Double = Double.pi  // 3.141592653589793
``` 
<br>


##### 2. Calculate the average of <code class="highlighter">x</code> and <code class="highlighter">y</code>.

```swift
let x: Int = 70
let y: Int = 60
let average = (x+y)/2    // 65
```
<br>


##### 3.1 Calculate the average of <code class="highlighter">x</code> and <code class="highlighter">y</code>, and solve the decimal point problem.

```swift
let averageFixed = Double((x+y))/2    // 65.0
```
<br>


##### 3.2 Explain the difference between (10/3) and (10.0/3.0).

```swift
// 計算 10/3 將會回傳一個整數 Int 型態
// 計算 10.0/3.0 將會回傳帶有小數點的浮點數 Double 型態

let average = 10/3               // 3
let averageFixed = 10.0/3.0      // 3.33333333...

print(type(of: average))         // Int
print(type(of: averageFixed))    // Double
```
<br>


##### 4. Change the following codes into the one with the data type.

```swift
var flag: Bool = true
var inputString: String = "Hello World."
let bitsInBite: Int = 8
let averageScore: Double = 86.8
```
<br>


##### 5. Please create a salary as 22000, and use unary plus operator adding 28000 to salary, and it will be 50000 after this process.

```swift
var salary = 22000
salary += 28000

print(salary)    // 50000
```
<br>


##### 6. Please write down the Equality operator in swift.

```swift
// Equality operator in Swift is '=='

1 == 3    // false
```
<br>


##### 7. Declare two constants that values are <code class="highlighter">10</code> and <code class="highlighter">3</code> each, then please calculate the remainder and save the result in a constant named <code class="highlighter">remainder</code>.
```swift
let x = 10
let y = 3
let remainder1 = x % y    // 1
let remainder2 = y % x    // 3
```
<br>


##### 8. Please explain the difference between let and var .
```swift
/* 

1. let 被用來宣告一個不可變的常數，數值只能在宣告時被初始化。
2. var 被用來宣告一個可變的變數，數值可在程式中被更動。

*/ 
```
<br>


##### 9. Please write down naming conventions and rules you learned in this session.
```swift
/*

1. 以小寫作為變數命名的開頭（如：petName）
2. 使用有意義、有描述性的名詞（如：daysOfTheWeek、studentName）
3. 避免使用無意義的代名詞或縮寫（如：x、y、dotw）
4. 在迴圈中的控制變數通常使用 i、j、k

*/
```
<br>


##### 10. What is Type Inference in swift?
```swift
// Type Inference（型別推斷）意指編譯器會自動偵測指派資料的型態，決定新變數的型態。以下舉例：

var studentName = "Chris"    // String
var studentAge = 16          // Int
var studentWeight = 47.5     // Double
var studentPassesd = true    // Bool
```
<br>


##### 11.  What is the problem about this piece of code?
```swift
// phoneNumber的型態在宣告時，因Type Inference被定義為 Int，而"Hello World." 的型態為字串（String），Swift 無法指派字串到Int 變數

var phoneNumber = 0987654321    
phoneNumber = "Hello World."    // Error: Cannot assign value of type 'String' to type 'Int'
```
<br>
<br>


> [2021-07-28 21:25 Yi-Chin Hsu]