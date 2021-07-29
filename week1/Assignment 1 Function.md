# Assignment 1: Function

<br>

#### Q1. Please declare a function named <code class="highlighter">greet</code> with <code class="highlighter">person</code> as argument label and <code class="highlighter">name</code> as a parameter name. This function will return a String. 

```swift
func greet(person name: String) -> String {
    return "Hello, \(name)"
}
greet(person: "Luke")    //Hello, Luke"
``` 

<br>


#### Q2. Please declare a function named <code class="highlighter">multiply</code> with two arguments <code class="highlighter">a</code> and <code class="highlighter">b</code> . This function won’t return any value and will only print out the result of <code class="highlighter">a * b</code> . Be noticed that we want to give argument <code class="highlighter">b</code> a default value of <code class="highlighter">10</code>.

```swift
func multiply(a: Double, b: Double = 10) {
    print(a*b)
}

multiply(a: 20)    // 200.0
``` 

<br>


#### Q3. What’s the difference between <code class="highlighter">argument label</code> and <code class="highlighter">parameter name</code> in function?

```swift
/*
 
 argument label 是外部在呼叫 function 時在（）內傳入的參數名稱。
 parameter name 是 function 內部存取的參數名稱。
 有效運用這兩個名稱，可以幫助我們寫出更符合閱讀語意的程式碼。
 
 */

func greet(person name: String) -> String {
//                 ^parameter label
    return "Hello, \(name)"
}
greet(person: "Luke")
//      ^argument name
``` 

<br>


#### Q4. What are the return types in the following statements?



```swift
func birthday() -> String {
    // birthday() is expected to return 'String'
}

func payment() -> Double {
    // payment() is expected to return 'Double'
}
``` 

<br>
<br>


> [2021-07-29 13:48 Yi-Chin Hsu]