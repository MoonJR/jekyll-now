# Swift3 정리
* ?가 붙은 변수(Optional 변수)와 안 붙은 변수는 다른 변수이다.

```swift
var x: String? = "안녕"	//?가 붙은 변수만 nil이 들어갈 수 있다.
var y: String = "안녕"
print(x);				//Optional("안녕")
print(y);				//안녕
print(x!);				//안녕

if x == y {				//같은 값이다.
    print("같은 값이다.")
}else{
    print("다른 값이다.")
}

print(x! + y) 			//안녕안녕
//print(x+y)			//Error --> Optional 변수를 연산할 때는 !를 붙혀야함.
```

* 빈 배열 혹은 Dictionary 형을 선언하는 방법

```swift
var array1 : [String] = []
var array2 = [String]()

var dic1 : [String:String] = [:]	//Dictionary에서 value 값은 기본 Optional 형으로 선언된다.
var dic2 = [String:String]()
var dic3 = [String:Any]()			//어떤 값도 들어갈 수 있음.
```

* 반복문 사용방법 

```swift
// 지정횟수 반복
for x in 0...5 {
  print(x) // 6번반복
}
 
for x in 0..<6 {
  print(x) // 6번반복
}
 
// 배열반복
var a = [1, 2, 3, 4, 5]
for value in a {
   print(value) 
}
 
var a = [1, 2, 3, 4, 5]
a.forEach { print($0) }
 
for (i, value) in a.enumerated() {
  print(i) // 배열 반복(인덱스포함)
}
 
var x = "abcde"
for(i, char) in x.characters.enumerated() {
   print(char) // 한글자씩 
} 
 
var a = [0: 10, 1: 20, 2: 30]
for(key, value) in a {
  print(key)
}
 
//while문
while(condition) {
 
}
 
//nil이외의 요소를 반복
var a: [String?] = ["1", nil, "2"]
for case let value? in a {
  print(value)
}
```

*Switch문 사용방법

```swift
var x = 100
switch x {
case 1:
  print("1")
case 60, 70: 
  print("60 또는 70")
case 85...99:
  print("85~99")
case 100:
  print("100")
default: 
  print("기타") 
}
```

