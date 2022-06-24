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
<br>
![image](https://user-images.githubusercontent.com/102133961/175230761-77844584-13be-4c7f-81e9-dbbf8c15a19e.png)<br>
 반복적으로 코드가 실행되게 만드는 구문<br>
프로그램을 작성하다 보면 같은 코드를 여러 번 호출해야 하는 경우가 생긴다<br>
for-in<br>
while<br>
repeat-while<br>
이 있다.<br>
<br>
<br>
/*<br>
for 루프상수 in 순회대상 {<br>
  // 실행할 구문...: 코드블럭<br>
}<br>
*/<br>
<br>
for i in 1...4 {<br>
print(i)<br>
}<br>
<br>
-> 1,2,3,4 차례대로 출력<br>
<br>
let array = [1,2,3,4,5]<br>
for i in array {<br>
 print(i)<br>
}<br>
<br>
이렇게 범위 데이터에 배열을 넣을 수 있다<br>
<br>
<br>
/*<br>
while 조건식 {<br>
  // 실행할 구문<br>
<br>
 }<br>
*/<br>
<br>
var number = 5<br>
while number < 10 {<br>
  number+=1<br>
}<br>
<br>
<br>
<br>
/*<br>
 repeat {<br>
  // 실행할 구문<br>
 } while 조건식<br>
*/<br>
<br>
var x = 6<br>
<br>
repeat {<br>
x+=2<br>
} while x < 5<br>
<br>
print(x)<br>
<br>
->적어도 한 번은 반드시 구문을 실행한다.<br>
<br>
<br>
![image](https://user-images.githubusercontent.com/102133961/175237335-0b7ec120-2c2b-4cde-a0d5-3ac27f7014ac.png)<br>
  값이 있을 수도 있고 없을 수도 있다<br>
(선택적인)<br>
<br>
var name: String=""<br>
이녀석은 값이 있는 걸까 없는 걸까<br>
<br>
정확히 말하자면 빈 문자열이라는 값을 갖고 있는 것이다.<br>
<br>
값이 없는 경우는 바로<br>
<br>
var name: String=nil<br>
<br>
이렇게 nil이 되는 것이다<br>
<br>
var number:Int? = nil<br>
<br>
이 경우도 마찬가지<br>
<br>
그렇다고 모든 경우에 nil을 넣을 수 있는 것이 아니라<br>
<br>
위의 경우와 같이 값이 있을수도 있고 없을 수도 있는 변수를 정의할 때<br>
타입 뒤에 ? 물음표를 붙여줘야 nil을 지정해줄 수 있다.<br>
<br>
이렇게 정의한 변수를 우리는 철수 아니 옵셔널이라고 부른다<br>
옵셔널의 경우 기본값은 nil이다<br><br>
<br>
일반적인 프로그래밍 언어에서는 값이 nil인 변수에 접근하면 런타임 에러가 발생해 프로그램이 종료된다 하지만 스위프트는 안전성 때문에 특이하게 값이 nil인 변수에 접근해도 프로그램이 종료되지 않는다.<br>
<br>
<br>
<br>
import UIKit<br>
<br>
var name: String?<br>
<br>
-> 이거 실행하면 그냥 nil 나옴<br>
<br>
그리고 옵셔널 타입에는 일반값도 넣을 수 있다<br>
<br>
var optionalName: String? = "Jinyong"<br>
<br>
// var requiredName: String = optionalName<br>
<br>
이런 경우 에러가 난다. requiredName은 옵셔널이 아닌 String타입이므로 값이 꼭 있어야 하고, optionalName이 옵셔널 타입이므로 이 녀석이 실행되기 전까지 값이 있나 없나를 모르기 때문 <br>
<br>
따라서 swift는 안전을 위해 이런 경우를 금지한다<br>
<br>
이때 발생하는 에러는 optionalName이라는 변수의 옵셔널 포장지를 벗기라는 에러가 뜨는데<br>
optionalName변수를 출력해 보면 Optional("Jinyong") 처럼 옵셔널 포장지에 싸여있는 것을 볼 수 있다.<br>
이 포장지를 벗겨주려면 옵셔널 바인딩을 이용해야만 한다.<br>
<br>
![image](https://user-images.githubusercontent.com/102133961/175237404-c47d5a23-93a0-4d45-b523-75f1ebfd5f1c.png)<br>
옵셔널 해제 방법에는 명시적 해제와 묵시적 해제가 있다<br>
  <img width="329" alt="image" src="https://user-images.githubusercontent.com/102133961/175237494-2021d5cb-d28d-40ec-9678-a1c32f1142a2.png"><br>
먼저 명시적 해제하는 두가지 방법부터 알아보도록 하자<br>
<br>
import UIKit<br>
<br>
var number: Int? = 3<br>
print(number)<br>
print(number!)<br>
<br>
실행해 보면 <br>
<br>
Optional(3)<br>
3<br>
<br>
이렇게 나온다.<br>
옵셔널 변수에 느낌표를 붙여주면 강제로 옵셔널이 해제된 것을 볼 수 있는데<br>
이 방법은 상당히 위험하다<br>
<br>
옵셔널을 강제 해제 하게 되면, 에러가 발생해 프로그램이 종료될 수도 있다.<br>
<br>
그렇다면 조금 더 안전한 방법은 없을까?<br>
<br>
옵셔널을 조금 더 안전하게 추출하려면 '비 강제 해제-옵셔널 바인딩'을 하면 된다.<br>
<br>
if let result = number {<br>
  print(result)<br>
}else{<br><br>
<br>
}<br>
<br>
옵셔널 타입의 값을 변수 또는 상수로 할당하는 구문이다.<br>
옵셔널이 벗겨지면 print가 실행되고 옵셔널 추출에 실패하면 else구문이 실행된다<br>
->그래서 묶어준다고 해서 바인딩이라고 부른다<br>
옵셔널 바인딩은 guard문으로도 가능한데<br>
<br>
func test(){<br>
  let number: Int? = 5<br>
  guard let result = number else {return}<br>
  print(result)<br>
}<br>
<br>
test()<br>
<br>
이렇게 하면 추출됨<br>
<br>
if를 이용해 옵셔널 바인딩을 하면 옵셔널이 추출된 변수나 상수를 if 블록 내에서만 사용할 수 있지만, guard문으로 옵셔널을 추출하면 <br>guard문 다음 함수 전체 구문에서 사용할 수 있다.<br>
<br>
guard문은 guard문 조건을 만족할 때만 guard문을 통과하고(그래서 guard문: 장벽같은 녀석) 만약 통과하지 못한다면 else문으로 나간다(흐름을 종료시킨다) : 이후에 더 자세히 다룰 예정<br>
<br>
다음은 묵시적 해제를 이용해 옵셔널을 벗겨볼 것이다.<br>
<br>
먼저 컴파일러에 의한 자동해제가 있다<br>
<br>
옵셔널 값을 비교연산자를 이용해 다른 값과 비교하면 컴파일러가 자동적으로 옵셔널을 해제시켜주는 것이다.<br>
<br>
let value: Int? = 6<br>
if value == 6 {<br>
  print("value가 6입니다")<br>
 } else {<br>
  print("value가 6이 아닙니다")<br>
}<br>
<br>
-> value가 6입니다<br>
출력<br>
<br>
이처럼 다른 값과 옵셔널 값을 비교해주면 컴파일러가 알아서 해제시켜준다.<br>
<br>
마지막으로 묵시적 옵셔널 해제에 대해 알아보자<br>
묵시적 해제는 옵셔널 타입이지만 값을 사용할 때는 자동으로 옵셔널이 해제된다<br>
<br>
let string = "12"<br>
var stringToInt: Int? = Int(string) //여기서 string 변수가 한글이나 다른 문자일 수도 있어서 이런 경우 nil을 반환하기 때문에 Int(string)의 반환 타입은 옵셔널이다. <br>
//print(stringToInt + 1)<br>
<br>
<br>
let string = "12"<br>
var stringToInt: Int! = Int(string) <br>
print(stringToInt + 1)<br>
<br>
이렇게 stringToInt 변수의 타입 뒤에 느낌표를 붙여주게 되면, 묵시적 옵셔널 해제가 일어난다. 타입 뒤에 느낌표가 붙여져 있는 옵셔널 변수는 자동적으로 옵셔널 해제가 일어나 일반값처럼 자유롭게 사용할 수 있다<br>
<br>

![image](https://user-images.githubusercontent.com/102133961/175473934-69dd03b3-a17d-4924-905f-455f8f52845a.png)<br>
프로퍼티와 메소드를 이용해 구조화된 틀을 만든다<br>
지겹도록 봐왔다<br>
<br>
하나의 새로운 사용자 정의 데이터 타입을 만들어 준다고 생각하면 쉽다<br>
<br>
또는 붕어빵 틀을 만든다고 생각하면 쉽다<br>
<br>
스위프트에서도 구조체와 클래스 사용 방식도 거의 동일한데<br>
<br>
약간의 차이점이 존재한다<br>
<br>
클래스의 인스턴스는 참조타입<br>
구조체의 인스턴스는 값 타입이라는 점이다<br>
<br>
struct 구조체 이름 {<br>
프로퍼티와 메소드<br>
}<br>
<br>
import UIKit<br>
<br>
struct User {<br>
var nickname: String<br>
var age: Int<br>
<br>
func information(){<br>
print("\(nickname) \(age)")<br>
  }<br>
}<br>
<br>
var user = User(nickname: "Jinyong", age: 23)  //생성자로 값을 초기화: 디폴트 생성자<br>
<br>
user.nickname // 프로퍼티에 접근<br>
<br>
user.nickname = "alphago" // 프로퍼티 값 변경<br>
<br>
user.information() // 구조체 함수(메소드)에 접근<br>
<br>
클래스는 클래스 키워드로 정의한다<br>
<br>
class 클래스 이름 {<br>
  프로퍼티와 메소드<br>
}<br>
<br>
import UIKit<br>
<br>
class Dog {<br>
var name: String = ""<br>
var age: Int = 0<br>
<br>
func introduce(){<br>
  print("name \(name) age \(age)")<br>
  }<br>
}<br>
<br>
var dog = Dog() // 인스턴스 생성<br>
dag.name = "coco"<br>
dog.age = 3<br>
dog.age<br>
<br>
dog.introduce()<br>
<br>
![image](https://user-images.githubusercontent.com/102133961/175474002-aaa9c1bb-2942-442d-ad0a-0bb8c241d1bd.png)<br>
클래스 구조체 또는 열거형의 인스턴스를 사용하기 위한 초기 과정<br>
->생성자<br>
<br>
프로퍼티 초기화 및 필요한 조정 수행 역할<br>
<img width="228" alt="image" src="https://user-images.githubusercontent.com/102133961/175474051-3df6d914-8772-46a5-9a03-23091be68cf1.png"><br>
위 사진에서 user 상수를 실행할 때, init이 호출되어 초기화 구문이 정의되어 있다면 초기화된다.<br>
<br>
방식은<br>
<br>
init(매개변수: 타입, ...) {<br>
  // 프로퍼티 초기화<br>
  // 인스턴스 생성시 필요한 설정을 해주는 코드 작성<br>
}<br>
<br>
ex)<br>
<br>
class User {<br>
<br>
  var nickname: String<br>
  var age: Int<br>
<br>
  init(nickname: String, age: Int) {<br>
<br>
 self.nickname=nickname<br>
self.age = age <br>
  }<br>
<br>
init(age: Int) {<br>
  self.nickname = "albert"<br>
  self.age =age<br>
  }<br>
 }<br>
}	<br>
<br>
var user = User(nickname: "jinyong", age: 23)<br>
user.nickname<br>
user.age<br>
<br>
var user2 = User(age: 27)
user2.nickname
user2.age
<br>
생성자와 반대되는 소멸자(Deinitializer)도 있다
<br>
메모리 정리 및 삭제 기능을 구현할 수 있다<br>
<br>
deinit {<br>
  print("deint user")<br>
 }<br>
}<br>
<br>
인스턴스가 있어야지 사용가능하다<br>
인스턴스가 더이상 필요하지 않다면 인스턴스에 nil을 집어넣어라<br>
그러면 더이상 인스턴스가 필요하지 않다고 판단해<br>
deinit이 호출된다.<br>
<br>
![image](https://user-images.githubusercontent.com/102133961/175483146-ffc15bc5-7e9f-4492-97c7-78ab22426da8.png)<br>
프로퍼티는 클래스, 또는 열거형 등에 변수처럼 있는 값<br>
프로퍼티는 세 가지 종류를 가진다<br>
저장 프로퍼티<br>
연산 프로퍼티<br>
타입 프로퍼티<br>
<br>
먼저 저장 프로퍼티는 프로퍼티를 사용하는 가장 간단한 방법이다<br>
struct Dog {<br>
 var name: String<br>
 let gender: String<br>
<br>
}<br>
<br>
var dog = Dog(name:"warwar", gender: " Male")<br>
print(dog)<br>
<br>
이렇게 프로퍼티에 값을 저장시키는 것을 저장 프로퍼티라고 한다<br>
dog.name = "윤진용"<br>
let dog2 = Dog(name: "warwar", gender: "Male")<br>
dog2.name = "윤진용" // 에러 발생<br>
<br>
이 경우에는 dog2 즉 인스턴스 변수가 상수로 선언되어 있어서<br>
프로퍼티 값의 변경이 불가능하다<br>
<br>
이러한 결과가 나온 이유는 구조체가 값 타입이기 때문이다.<br>
구조체 인스턴스를 상수로 선언하면 내부 프로퍼티도 상수화되어 변경이 불가능해진다.<br>
<br>
그렇다면 클래스는 어떨까?<br>
<br>
클래스는 참조타입이라 구조체와는 조금 다른 결과가 나온다.<br>
<br>
클래스 인스턴스는 상수로 선언해도 변수로 선언한 프로퍼티 값을 변경할 수 있다.<br>
<br>
class Cat {<br>
<br>
var name: String<br>
let gender: String<br>
init(name: String, gender: String){<br>
  self.name = name<br>
  self.gender = gender<br>
  }<br>
}<br>
<br>
let cat = Cat(name: "json", gender: "female")<br>
cat.name = "jonson"<br>
print(cat.name)<br>
<br>
클래스는 참조 타입이기 때문에 인스턴스를 상수로 선언했다 하더라도 내부 변수 타입 프로퍼티 값의 변경이 가능하다. 하지만 당연히 gender같은 상수 타입 프로퍼티는 변경할 수 없다. <br>
<br>
다음으로 연산 프로퍼티에 대해 알아보자,<br>
<br>
저장 프로퍼티는 구조체와 클래스에서만 사용 가능했지만<br>
연산 프로퍼티는 열거형에서도 사용할 수 있다.<br>
<br>
연산 프로퍼티는 값을 직접적으로 저장하지 않는 대신 getter 와 setter 를 이용해서 값을 직접적으로 접근하고 수정할 수 있다.<br>
<br>
struct Stock {<br>
  var averagePrice: Int<br>
  var quantity: Int<br>
  var purchasePrice: Int {<br>
     get {<br>
      return averagePrice * quantitiy<br>
     }<br>
<br>
     set(newPrice){<br>
       averagePrice = newPrice / quantity<br>
      }<br>
   }<br>
}<br>
<br>
<br>
var stock = Stock(averagePrice: 2300, quantity: 3)<br>
print(stock)<br>
stock.purchasePrice -> 6900 // get 실행<br>
stock.purchasePrice = 3000 // set 실행<br>
stock.averagePrice -> 1000<br>
<br>
참고로 set만 지워서 읽기 전용 프로퍼티로 만들 수 있다<br>
이런 경우 값을 변경할 수 없게 된다<br>
그리고 set을 설정할 때 매개변수 디폴트 값은 newValue이다<br>
<br>
그 다음으로 프로퍼티 옵저버를 살펴보겠다<br>
<br>
프로퍼티 옵저버는 프로퍼티 값의 변화를 살펴보고 반응한다.<br>
<br>
새로운 값이 기존 값과 같더라도 프로퍼티 옵저버는 실행된다.<br>
<br>
프로퍼티가 set될 때마다 호출된다고 보면 된다.<br>
<br>
프로퍼티 옵저버는 세 가지 경우에만 사용할 수 있다<br>
저장 프로퍼티랑 오버라이딩이 된 저장 연산 프로퍼티에서만 사용할 수 있다.<br>
<br>
class Account {<br>
 var credit: Int = 0 {<br>
  <br>
  willSet {<br>
    print("잔액이 \(credit)원에서 \(newValue)원으로 변경될 예정입니다.")<br>
      }<br>
   didSet {<br>
 print("잔액이 \(oldValue)원에서 \(credit)원으로 변경되었습니다.")<<br>
     }<br>
  }<br>
}<br>
<br>
var account = Account()<br>
account.credit = 1000<br>
->잔액이 0원에서 1000원으로 변경될 예정입니다<br>
  잔액이 0원에서 1000원으로 변경되었습니다.<br>
willSet이나 didSet이나 모두 매개변수를 지정할 수 있는데 지정하지 않는다면<br>
newValue와 oldValue가 디폴트 매개변수가 된다. <br>
  <br>
<br>
마지막으로 타입 프로퍼티는 인스턴스 생성 없이 객체 내 프로퍼티에 접근 할 수 있도록 하는 거다<br>
<br>
프로퍼티 타입 자체와 연결하는 것이다.<br>
저장 프로퍼티와 연산 프로퍼티에서만 사용 가능하다.<br>
static 키워드를 사용해서 정의한다.<br>
<br>
struct SomeStructure {<br>
  static var storedTypeProperty = "Some value."<br>
  static var computedTypeProperty: Int {<br>
   return 1<br>
  }<br>
}<br>
<br>
static이라 그냥 인스턴스 생성 안하고 바로 타입으로 호출할 수 있다. (전역_)<br>
SomeStructure.computedTypeProperty<br>
SomeStructure.storedTypeProperty<br>
SomeStructure.storedTypeProperty = "hello"<br>
값도 변경할 수 있다<br>



  
