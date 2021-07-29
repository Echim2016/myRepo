# Assignment 1: Control Flow

<br>

#### Q1. Please use For-Loop and Range to print the last three members in the <code class="highlighter">lottoNumbers</code> array.

```swift
let lottoNumbers = [10, 9, 8, 7, 6, 5]
for i in lottoNumbers.count-3..<lottoNumbers.count {
    print(lottoNumbers[i])
}

/* 顯示如下

7
6
5

*/
``` 

<br>


#### Q2. Please use swift syntax to get the result as images list below :

```shell
5
6
7
8
9
10
```

```shell
10
8
6
```
<br>

#### Q2.1. Using <code class="highlighter">for</code> loop to solve the above question.

```swift
for i in 0..<lottoNumbers.count {
    print(lottoNumbers[lottoNumbers.count-i-1])
}

/* 顯示如下

5
6
7
8
9
10

*/
``` 
<br>


#### Q2.2. Using <code class="highlighter">for</code> loop to solve the above question.

```swift
for i in 0..<lottoNumbers.count where lottoNumbers[i] % 2 == 0 {
    print(lottoNumbers[i])
}

/* 顯示如下

10
8
6

*/
``` 
<br>


#### Q3.1. Using <code class="highlighter">while</code> loop to solve the above question.

```swift
var i = 0
while i < lottoNumbers.count {
//    print(lottoNumbers[lottoNumbers.count-i-1])
    i += 1
}

/* 顯示如下

5
6
7
8
9
10

*/
``` 
<br>


#### Q3.2. Using <code class="highlighter">while</code> loop to solve the above question.

```swift
var i = 0
while i < lottoNumbers.count {
    if lottoNumbers[i] % 2 == 0 {
        print(lottoNumbers[i])
    }
    i += 1
}

/* 顯示如下

10
8
6

*/
``` 
<br>


#### Q4.1. Using <code class="highlighter">repeat-while</code> loop to solve the above question.

```swift
var i = 0
repeat {
    print(lottoNumbers[lottoNumbers.count-i-1])
    i += 1
} while i < lottoNumbers.count

/* 顯示如下

5
6
7
8
9
10

*/
``` 
<br>


#### Q4.2. Using <code class="highlighter">repeat-while</code> loop to solve the above question.

```swift
var i = 0
repeat {
    if lottoNumbers[i] % 2 == 0 {
        print(lottoNumbers[i])
    }
    i += 1
} while i < lottoNumbers.count

/* 顯示如下

10
8
6

*/
``` 
<br>


#### Q5. What are the differences between <code class="highlighter">while</code> and <code class="highlighter">repeat-while</code> ?

```swift
/* 

while 在進入迴圈前就先檢查進入條件是否符合，
檢查後才會決定是否進入迴圈執行，
而 repeat-while 則是在迴圈執行後才檢查，
因此無論如何都會先執行一次迴圈。

*/
``` 
<br>


#### Q6. Here is the variable <code class="highlighter">isRaining</code> to record the weather. Please write a statement that if the weather is raining, print “It’s raining, I don’t want to work today.”, otherwise print “Although it’s sunny, I still don’t want to work today.”

```swift
var isRaining: Bool = true
if isRaining == true {
    print("It's raining, I dont want to work today.")
}
else {
    print("Although it's sunny, I still don't want to work today.")
}
``` 

```swift
// 或者，可利用 ternary operator 將其寫為：
print(isRaining ? "It's raining, I dont want to work today." : "Although it's sunny, I still don't want to work today.")    // It's raining, I dont want to work today
``` 
<br>


#### Q6. In a company, we usually use numbers to represent job levels. Let’s make an example. There are four job levels: Member, Team Leader, Manager, and Director. Now, create a variable name <code class="highlighter">jobLevel</code> and assign a number to it. If the <code class="highlighter">jobLevel</code> number is in our list, print the relative job title name; if not, just print “We don't have this job”. Please use a switch statement to complete this requirement.

```swift
var jobLevel = 3
switch jobLevel {
case 1:
    print("Member")
case 2:
    print("Team Leader")
case 3:
    print("Manager")
case 4:
    print("Director")
default:
    print("We don't have this job")
}

/* 顯示如下

Manager

*/
``` 

```swift
var jobLevel = 0
switch jobLevel {
case 1:
    print("Member")
case 2:
    print("Team Leader")
case 3:
    print("Manager")
case 4:
    print("Director")
default:
    print("We don't have this job")
}

/* 顯示如下

We don't have this job

*/
``` 
<br>

<br>


> [2021-07-29 12:42 Yi-Chin Hsu]