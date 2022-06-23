# SWIFT_GRAMMAR
learn swift grammar

스위프트 기초 문법![image](https://user-images.githubusercontent.com/102133961/175220906-218a6a72-9580-40ac-a790-0824f2703bbc.png)

상수와 변수

프로그래밍에서 상수와 변수는 값을 메모리에 저장할 수 있는 일정한 저장 공간이라고 이해하면 된다. 각각 변하지 않는 일정한 값, 변할 수 있는 값을 나타낸다
쉽게 말해 상수는 어떠한 값을 넣어도 변하지 않는다
상수는 

let 상수명:데이터 타입 = 값

변수는

var 변수명:데이터 타입 = 값

이렇게 사용을 한다.

import Foundation

let a: Int = 100

//a = 200 이러면 에러->상수는 변경 불가능

var b: Int = 200

예를 들어 핸드폰의 전체 용량은 상수로 설정하고 사용 가능 공간을 변수로 설정한다.



스위프트의 기본 데이터 타입

Int : 64bit 정수형
UInt : 부호가 없는 64bit 정수형
Float: 32bit 부동 소수점 (Float 변수에 정수를 저장해도 자동으로 부동 소수점으로 변환)
Double : 64bit 부동 소수점
Bool : true, false 값
Character : 문자	
ex)
var someCharacter : Character = "가"

String : 문자열
Any: 모든 타입을 자칭하는 키워드(어떤 타입이든 다 가질 수 있다)

스위프트는 타입 추론을 할 수 있다

따라서 변수나 상수명 뒤에 특정 타입을 명시하지 않아도 컴파일러가 알아서 타입을 추론하여 타입을 결정해준다.

var number = 10

그냥 이렇게 써줘도 'Int형 타입이구나' 라고 추론한다


컬렉션 타입
컬렉션 타입은 데이터들의 집합 또는 묶음이다
스위프트의 컬렉션 타입에는 크게 Array, Dictionary, Set가 있다.
Array
데이터 타입의 값들을 순서대로 지정하는 리스트
우리가 흔히 아는 배열이다

Dictionary
키와 값의 쌍으로 데이터를 저장하는 컬렉션 타입

Set
같은 데이터 타입의 값을 순서 없이 저장하는 리스트
값 중복 허용 안 함
그냥 집합이라고 생각하자

자바와 자료구조 시간에 배운 것이기에 세부적인 사항은 넘어간다

import UIKit

var numbers: Array<Int> = Array<Int>()
numbers.append(1)
numbers.append(3)
numbers.append(2)

numbers[0]
numbers[1]
numbers.insert(4, at:2) // index 2번에 4를 집어넣음 
numbers
numbers.remove(at:0)
numbers

var names = [String]()
var names: [String] = []

//var dic: Dictionary<String, Int> = Dictionary<String, Int>()
var dic: [String: Int] = ["윤진용": 1]
dic["철수"] = 3
dic["김지"] = 5
dic

dic.removeValue(forKey: "김민지")

var set: Set = Set<Int>()
//set는 축약형 형태가 따로 없다!

set.insert(10)
set.insert(20)
set.insert(30)
set.insert(30)
set.insert(30)

set.remove(20)



함수
함수는 작업의 가장 작은 단위 그리고 코드의 집합이다
계속해서 중복되는 코드를 줄이기 위해 사용한다

func 함수명(파라미터 이름: 데이터 타입)->반환타입 {
return 반환값
}

func sum(a: Int, b: Int) -> Int {

return a+b

}

sum(a: 5, b: 3)


func hello() -> String { //매개변수 없는 함수

return "hello"

}

hello()

func printName() -> Void {
  // 반환 값 없는 함수
}

또는

func printName() {
 // 반환 값 없는 함수 
}

func greeting(friend: String, me: String = "jinyong"){
  print("Hello, \(friend)! I'm \(me)")
}

greeting(friend: "Albert")

//전달인자레이블 사용
func sendMessage(from myName: String, to name: String) -> String{
return "Hello \(name)! I'm \(myName)"
}

sendMessage(from: "Gunter", to: "Json")

//와일드카드(바로 값 넘겨주기)

func sendMessage(_ name: String) -> String {
return "Hello \(name)"

}

sendMessage("윤진용")

//가변매개변수

func sendMessage(me: String, friends: String. . .) -> String {
  return "Hello \(friends)! I'm \(me)"
}

sendMessage(me: "Jinyong", friends: "Jonson", "aiensert", "serius")

가변 매개변수로 선언되어 있으면 배열을 받을 수 있다고 생각하면 쉽다

스위프트의 함수는 일급 객체이다. 그래서 함수를 변수로 할당 할 수도 있고 매개변수에 집어넣을 수도 있다.
![image](https://user-images.githubusercontent.com/102133961/175220946-c3c0d9bf-4644-4bca-bde9-773eaf541a66.png)

