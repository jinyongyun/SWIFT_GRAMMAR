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

