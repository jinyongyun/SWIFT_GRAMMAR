# SWIFT_GRAMMAR
learn swift grammar

![image](https://user-images.githubusercontent.com/102133961/175221027-27897abd-65aa-4322-8cc5-9bc4f2b5465a.png)

![image](https://user-images.githubusercontent.com/102133961/175221051-441196c1-9de6-4f06-87ce-6d16e5338a35.png)

프로그래밍에서 상수와 변수는 값을 메모리에 저장할 수 있는 일정한 저장 공간이라고 이해하면 된다. 각각 변하지 않는 일정한 값, 변할 수 있는 값을 나타낸다<br>
쉽게 말해 상수는 어떠한 값을 넣어도 변하지 않는다<br>
상수는 <br>

let 상수명:데이터 타입 = 값<br>

변수는<br>

var 변수명:데이터 타입 = 값<br>

이렇게 사용을 한다.<br>

import Foundation<br>

let a: Int = 100<br>

//a = 200 이러면 에러->상수는 변경 불가능<br>

var b: Int = 200<br>

예를 들어 핸드폰의 전체 용량은 상수로 설정하고 사용 가능 공간을 변수로 설정한다.<br>

![image](https://user-images.githubusercontent.com/102133961/175221183-e15b2ae1-364a-4945-9a74-a6385458ef4e.png)
<br>
Int : 64bit 정수형<br>
UInt : 부호가 없는 64bit 정수형<br>
Float: 32bit 부동 소수점 (Float 변수에 정수를 저장해도 자동으로 부동 소수점으로 변환)<br>
Double : 64bit 부동 소수점<br>
Bool : true, false 값<br>
Character : 문자	<br>
ex)<br>
var someCharacter : Character = "가"<br>
<br>
String : 문자열<br>
Any: 모든 타입을 자칭하는 키워드(어떤 타입이든 다 가질 수 있다)<br>
<br>
스위프트는 타입 추론을 할 수 있다<br>
<br>
따라서 변수나 상수명 뒤에 특정 타입을 명시하지 않아도 컴파일러가 알아서 타입을 추론하여 타입을 결정해준다.<br>
<br>
var number = 10<br>
<br>
그냥 이렇게 써줘도 'Int형 타입이구나' 라고 추론한다<br>
<br>

![image](https://user-images.githubusercontent.com/102133961/175221357-30431e78-bdd1-47b7-b51c-72ac3ff64b84.png)
<br>
컬렉션 타입은 데이터들의 집합 또는 묶음이다<br>
스위프트의 컬렉션 타입에는 크게 Array, Dictionary, Set가 있다.<br>
Array<br>
데이터 타입의 값들을 순서대로 지정하는 리스트<br>
우리가 흔히 아는 배열이다<br>
<br>
Dictionary<br>
키와 값의 쌍으로 데이터를 저장하는 컬렉션 타입<br>
<br>
Set<br>
같은 데이터 타입의 값을 순서 없이 저장하는 리스트<br>
값 중복 허용 안 함<br>
그냥 집합이라고 생각하자<br>
<br>
자바와 자료구조 시간에 배운 것이기에 세부적인 사항은 넘어간다<br>
<br>
import UIKit<br>
<br>
var numbers: Array<Int> = Array<Int>()<br>
numbers.append(1)<br>
numbers.append(3)<br>
numbers.append(2)<br>
<br>
numbers[0]<br>
numbers[1]<br>
numbers.insert(4, at:2) // index 2번에 4를 집어넣음 <br>
numbers<br>
numbers.remove(at:0)<br>
numbers<br>
<br>
var names = [String]()<br>
var names: [String] = []<br>
<br>
//var dic: Dictionary<String, Int> = Dictionary<String, Int>()<br>
var dic: [String: Int] = ["윤진용": 1]<br>
dic["철수"] = 3<br>
dic["김지"] = 5<br>
dic<br>
<br>
dic.removeValue(forKey: "김민지")<br>
<br>
var set: Set = Set<Int>()<br>
//set는 축약형 형태가 따로 없다!<br>
<br>
set.insert(10)<br>
set.insert(20)<br>
set.insert(30)<br>
set.insert(30)<br>
set.insert(30)<br>
<br>
set.remove(20)<br>

  ![image](https://user-images.githubusercontent.com/102133961/175221543-996cdcfc-2aab-4193-b7a1-469c2dbaefac.png)
<br>
  
  
함수는 작업의 가장 작은 단위 그리고 코드의 집합이다<br>
계속해서 중복되는 코드를 줄이기 위해 사용한다<br>
<br>
func 함수명(파라미터 이름: 데이터 타입)->반환타입 {<br>
return 반환값<br>
}<br>
<br>
func sum(a: Int, b: Int) -> Int {<br>
<br>
return a+b<br>
<br>
}<br>
<br>
sum(a: 5, b: 3)<br>
<br>
<br>
func hello() -> String { //매개변수 없는 함수<br>
<br>
return "hello"<br>
<br>
}<br>
<br>
hello()<br>
<br>
func printName() -> Void {<br>
  // 반환 값 없는 함수<br>
}<br>
<br>
또는<br>
<br>
func printName() {<br>
 // 반환 값 없는 함수 <br>
}<br>
<br>
func greeting(friend: String, me: String = "jinyong"){<br>
  print("Hello, \(friend)! I'm \(me)")<br>
}<br>
<br>
greeting(friend: "Albert")<br>
<br>
//전달인자레이블 사용<br>
func sendMessage(from myName: String, to name: String) -> String{<br>
return "Hello \(name)! I'm \(myName)"<br>
}<br>
<br>
sendMessage(from: "Gunter", to: "Json")<br>
<br>
//와일드카드(바로 값 넘겨주기)<br>
<br>
func sendMessage(_ name: String) -> String {<br>
return "Hello \(name)"<br>
<br>
}<br>
<br>
sendMessage("윤진용")<br>
<br>
//가변매개변수<br>
<br>
func sendMessage(me: String, friends: String. . .) -> String {<br>
  return "Hello \(friends)! I'm \(me)"<br>
}<br>
<br>
sendMessage(me: "Jinyong", friends: "Jonson", "aiensert", "serius")<br>
<br>
가변 매개변수로 선언되어 있으면 배열을 받을 수 있다고 생각하면 쉽다<br>
<br>
스위프트의 함수는 일급 객체이다. 그래서 함수를 변수로 할당 할 수도 있고 매개변수에 집어넣을 수도 있다.<br>
<br>
<br>
![image](https://user-images.githubusercontent.com/102133961/175224652-d1e4cd90-3281-4d28-bd6b-e7ae517d6621.png)<br>
주어진 조건에 따라 다르게 동작하도록 하는 문<br>
<br>
if, switch, guard 문이 있다<br>
<br>
import UIKit<br>
<br>
/*<br>
if 조건식 {<br>
 실행할 구문<br>
}<br>
*/<br>
<br>
let age = 12<br>
<br>
if age < 19 {<br>
  print("미성년자 입니다.")<br>
}<br>
<br>
/*<br>
 if 조건식 {<br>
  조건식이 만족하면 해당 구문 실행<br>
} else {<br>
만족하지 않는다면 해당 구문 실행<br>
}<br>
*/<br>
<br>
if age < 19 {<br>
  print("미성년자")<br>
} else {<br>
  print("성년자")<br>
}<br>
<br>
/* <br>
if 조건식1 {<br>
   // 조건식1을 만족할 때 실행할 구문<br>
} else if 조건식1 {<br>
 //조건식2를 만족할 때 실행할 구문<br>
} else {<br>
  // 아무 조건식도 만족하지 않을 때 실행할 구문<br>
}<br>
*/<br>
<br>
let animal = "cat"<br>
<br>
if animal == "dog" {<br>
  print("강아지 사료주기")<br>
} else if animal == "cat" {<br>
 print("고양이 사료주기")<br>
} else {<br>
  print("해당하는 동물 사료가 없음")<br>
}<br>
<br>
/* <br>
switch 비교대상 {<br>
<br>
case 패턴1:<br>
  // 패턴1 일치할 때 실행되는 구문<br>
case 패턴2, 패턴3:<br>
 // 패턴2, 3가 일치할 때 실행되는 구문<br>
default:<br>
 // 어느 비교 패턴과도 일치하지 않을 때 실행되는 구문<br>
}<br>
*/<br>
<br>
let color = "green"<br>
<br>
switch color {<br>
case " blue":<br>
  print("파란색 입니다")<br>
<br>
case "green":<br>
  print("초록색 입니다")<br>
<br>
case "yellow":<br>
  print("노랑색 입니다")<br>
<br>
default:<br>
  print("찾는 색상이 없습니다")<br>
}<br>
<br>
<br>
<br>
let temperature = 30<br>
<br>
switch temperature {<br>
<br>
case -20...9:<br>
 print("겨울 입니다")<br>
<br>
case 10...14:<br>
 print("가을 입니다")<br>
<br>
case 15...25<br>
  print("봄 입니다")<br>
<br>
case 26...35<br>
  print("여름 입니다")<br>
<br>
default:<br>
  print("이상 기후입니다")<br>
<br>
