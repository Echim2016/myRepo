# Assignment 1: Collection

<br>

##### Q1. Please create an empty array with  <code class="highlighter">String</code> data type and save it in a variable named <code class="highlighter">myFriends</code>.
```swift
var myFriends: [String] = []
``` 
<br>


##### Q2. According to Q1, now I have three friends, <code class="highlighter">'Ian'</code>, <code class="highlighter">'Bomi'</code>, and <code class="highlighter">'Kevin'</code>. Please help me to add their name into <code class="highlighter">myFriends</code> array.

```swift
myFriends += ["Ian", "Bomi", "Kevin"]
```
<br>


##### Q3. Please help me to add Michael to the end of <code class="highlighter">myFriends</code> array.


```swift
myFriends.append("Michael")
```
<br>


##### Q4. Please move Kevin to the beginning of the <code class="highlighter">myFriends</code> array.


```swift
myFriends.remove(at: 2)
myFriends.insert("Kevin", at: 0)
print(myFriends)    // ["Kevin", "Ian", "Bomi", "Michael"]


if let index = myFriends.firstIndex(of: "Kevin") {
   myFriends.remove(at: index)
   myFriends.insert("Kevin", at: 0)
}
```

```swift
// 若不知道 Kevin 的具體位置，亦可利用 firstIndex 找到Kevin的位置後刪除並新增到首位

if let index = myFriends.firstIndex(of: "Kevin") {
   myFriends.remove(at: index)
   myFriends.insert("Kevin", at: 0)
}
print(myFriends)    // ["Kevin", "Ian", "Bomi", "Michael"]

```
<br>


##### Q5. Use for...in to print all the friends in <code class="highlighter">myFriends</code> array.


```swift
for friend in myFriends{
    print(friend)   
}

/* 顯示如下
Kevin
Ian
Bomi
Michael
*/
```
<br>


##### Q6. Now I want to know who is at index <code class="highlighter">5</code> in the <code class="highlighter">myFriends</code> array, try to find the answer for me. Please explain how you get the answer and why the answer is it.


```swift
/* 
編譯器將會出現錯誤，無法獲得答案。
由於 myFriends 的長度只有 4 ，因此 index 大於 3 的檢索都會造成 Index out of range 的嚴重錯誤。
*/

print(myFriends[5])    // Fatal error: Index out of range
```
<br>


##### Q7. How to get the first element in an array?


```swift
myFriends.first    // "Kevin"
```
<br>


##### Q8. How to get the last element in an array?


```swift
myFriends.last    // "Michael"
```
<br>


##### Q9. Please create a dictionary with keys of type <code class="highlighter">String</code>, value of type <code class="highlighter">Int</code>, and save it in a variable named <code class="highlighter">myCountryNumber</code>.


```swift
var myCountryNumber: [String: Int] = [:]
```
<br>


##### Q10. Please add three keys <code class="highlighter">'US'</code>, <code class="highlighter">'GB'</code>, <code class="highlighter">'JP'</code> with values <code class="highlighter">1</code>, <code class="highlighter">44</code>, <code class="highlighter">81</code>.


```swift
myCountryNumber = ["US" : 1, "GB" : 44, "JP" : 81]
```
<br>


##### Q11. Change the <code class="highlighter">'GB'</code> value from <code class="highlighter">44</code> to <code class="highlighter">0</code>.


```swift
myCountryNumber.updateValue(0, forKey: "GB")
```
<br>


##### Q12. How to declare an empty dictionary?


```swift
// Dictionary 可以使用以下兩種宣告方式：
var emptyDictionary: [keyType: valueType] = [:]
var emptyDictionary: Dictionary<keyType, valueType>

// 以本題 myCountryNumber 為例
var myCountryNumber: [String: Int] = [:]
var myCountryNumber: Dictionary<String, Int>
```
<br>


##### Q13. How to remove a key-value pair in a dictionary?


```swift
// 方法1：使用 removeValue (forKey:)：
    myCountryNumber.removeValue(forKey: "JP")
    print(myCountryNumber)    // ["GB": 0, "US": 1]

// 方法2：將欲刪除的 Key 指向 nil：
    myCountryNumber["JP"] = nil
    print(myCountryNumber)    //["GB": 0, "US": 1]
```
<br>

<br>


> [2021-07-28 23:03 Yi-Chin Hsu]