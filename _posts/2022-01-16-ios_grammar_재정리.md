import UIKit

import Darwin

import Foundation

import os

var greeting = "Hello, playground"

for i in 0...99{
    i
}

for i in 0...99{
    print(i)
}

//변수 : 사용 공간에 사용될 수 있다.

//var 변수명: 데이터 타입 = 값

var b:Int = 300

b=400

//데이터 타입

//int :  정수형

//Uint: 부호가 없는 정수형

//Float, Double, Bool, Character, String

//Any: 모든 타입을 지칭할 수 있다.

var someUint:UInt = 300

someUint = 200

var someFloat:Float = 1.1

someFloat = 1

print(someFloat)

var someDouble: Double = 1.1

someDouble = 1

print(someDouble)

var someBool:Bool = true

someBool = false

print(someBool)

//다음과 같이 초기화 안하고 시작해도 된다. -> 다른 언어와 같은 성질임

var someCharacter:Character

someCharacter = "A"

someCharacter = "s"

var someString:String = "안녕하세요"

//타입 추론(중요)

var string = "안녕!"

print(string)

//컬렉션 타입(중요) : array,dictionary,set

//Array :var 변수명:Array<변수타입>=Array<변수타입>()

var numbers: Array<Int> = Array()

numbers.append(1)

numbers.append(2)

numbers.append(3)

numbers[0]

numbers[1]

//insert하는 방법

numbers

numbers.remove(at:0)

numbers

//간단하게 배열을 정의하는 방법

var names:[String] = []

var number_2:[Int] = []

number_2.append(1)

number_2.append(2)

number_2.append(3)

number_2

//Dictionary

//var dic:Dictionary<String,Int>=Dictionary<String,Int>()

var dic:[String:Int]=[:]

dic["남궁광"] = 28

dic["박성린"] = 26

dic["김태현"] = 24

dic

dic.removeValue(forKey: "남궁광")

dic

dic.removeValue(forKey: "박성린")

dic

//Set은 축약형이 없다.

var set:Set<Int> = Set()

set.insert(10)

set.insert(20)

set.insert(30)

set

//함수는 작업의 가장 작은 단위이자 코드의 집합이다.

//func 함수명(파라미터이름:데이터 타입)->반환 타입{return 반환 값}

func sum(a:Int,b:Int)->Int{
    return a+b
}

sum(a:3,b:56)

func hello()->String{
    return "Hello kitty"
}

hello()

func greeting(friend:String,me:String="jacky"){
    print("Hello,\(friend)! I'm \(me)")
}

greeting(friend:"Taehyeon")

/*
 func 함수이름(전단인자 레이블:매개변수 이름:매개변수타입,전달인자 레이블:매개변수 이름:매개변수 타입...)->반환타입
 {
    return 반환 값
 }
 */

//변형 코드 보기:

func sendMessage(from name:String,to myname:String)
{
    print("Hello! \(name)! My name is \(myname)")
}

sendMessage(from: "Jacky", to: "TaeHyeon")

//조건문

//주어진 조건에 따라서 애플리케이션을 다르게 동작하도록 하는 것이다.

//if,switch,gurad

/*
 if 조건식{
    실행할 구문
 }
 */

//상수 선언

let age:Int = 20

if age<19{
    print("미성년자이다.")
}


if age<19{
    print("미성년자이다.")
}else{
    print("성년자이다.")
}

//if-else if-else

let animal = "cat"

if animal=="dog"{
    print("강아지")
}else if animal=="cat"{
    print("고양이")
}else{
    print("모릅니다.")
}


//switch문

/*
 switch 비교대상
 {
    case 패턴1:
    //패턴1 일치 될 때 실행 되는 구문
 
    case 패턴2:
    //패턴2 일치 될 때 실행 되는 구문
 
    case 패턴3:
    //패턴3 일치 될 때 실행 되는 구문
 
    default:
    //어느 비교패턴과도 일치하지 않을 때 실행되는 구문
 }
 */


let color = "green"

switch color{
case "blue":
    print("파란색")
    
case "green":
    print("초록색")
    
default:
    print("I don't know")

}

let temperature:Int = 30

switch temperature{
case -20...9:
    print("겨울")
    
case 10...14:
    print("가을")
    
case 15...25:
    print("봄")

case 26...35:
    print("여름")
    
default:
    print("이상기후 입니다")
}

//반복문 : 반복적으로 코드가 실행되게 만드는 구문을 말한다.

//for - in, while , repeat - while

/*
 for 루프상수 in 순회대상
 {
    실행구문..
 }
 */

for i in 1...4{
    print(i)
}

let array=["hacker","jacky","taylor"]

for i in array{
    print(i)
}

//while문이란 false 값이 나올 때 까지 사용하는 것이다.

var number_3 = 5

while number_3<10{
    number_3+=1
}

number_3

//do while문 같은 것이 repeat while 문이다.

/*
 repeat{
    //실행할 구문
 }while 조건식
 */

var x = 2

repeat{
    x+=2
}while x>10

print(x)

        
//옵셔널:값이 있을 수도 있고 없을 수도 있다.

var name:String? // 없는 경우는 nil값이 들어가 있다.

var optionalName:String? = "jacky"

print(optionalName) //옵셔널 값 안에서 출력이 됨.

//명시적 해제 : 강제해제

//옵셔널 바인딩: 비강제 해제

//묵시적 해제 (컴파일러에 의한 자동 해제, 옵셔널의 묵시적 해제)

//var requiredname:String = optionalName

var number_5: Int?=3

print(number_5)

//느낌표로 강제로 바인딩을 해제 할수 있지만 nil이 들어가 있을 때는 치명적인 오류가 나타날 수 있다.

print(number_5!)

//비강제로 바인딩을 해제해보겠다.

if let result = number_5{
    print(result)
}else{

}

//guard 문으로 옵셔널을 품

func test(){
    let number:Int?=5
    
    guard let result=number else{return}
    
    print(result)
    
}

test()

let value_2: Int? = 6

if value_2 == 6 {
    print("value가 6입니다.")
}else{
    print("value가 6이 아닙니다.")
}

//묵시적 해제

let string_2 = "12"

var stringToInt:Int!=Int(string_2)

print(stringToInt+1)

//클래스와 구조체 :참조 타입 /값 타입 ->참조 타입이 더 좋다..

//구조체
/*
 struct 구조체 이름
 {
 프로퍼티와 메서드
 }
 */

struct User{
    var nickname:String
    var age:Int
    
    func information(){
        print("\(nickname) \(age)")
    }
}

//인스턴트 생성

/*
var user=User(nickname: "jacky", age: 28)

user.nickname

user.nickname="taehyeon"

user.nickname

user.information()
*/

//클래스
/*
 class 클래스 이름{
    프로퍼티와 메서드
 }
 
 */

class User_2{
    var nickname:String=""
    
    var age:Int=0
    
    //생성자를 안만들면 자동으로 생성이 된다는 것을 이론적으로는 알고 있어야한다. also, 구조체도 마찬가지이다.
    
    init(nickname:String,age:Int){
        self.nickname = nickname
        
        self.age=age
    }
    
    init(age:Int)
    {
        self.nickname="Json"
        
        self.age=age
    }
    
    deinit{
        print("deinit이 출력 되었습니다.")
    }
    
    func introduce(){
        print("name: \(nickname) age:\(age) ")
    }
}

    

//초기화 선언 안하면 이렇게 해야한다.
/*
var dog=Dog()

dog.name="coco"

dog.age=3

dog.name

dog.age

dog.introduce()
 */

//초기화를 하였을 때

var user=User_2(nickname:"jacky",age:28)

user.nickname

user.age

var user2=User_2(age:29)

user2.nickname

user2.age

var user3:User_2? = User_2(age:23)

user3=nil

//프로퍼티: 클래스, 구조체 또는 열거형 등에 관련된 값을 뜻한다.

//저장 프로퍼티, 연산 프로퍼티, 타입 프로퍼티

//저장 프로퍼티

struct Dog_2{
    var name:String
    let gender:String
}

var dog=Dog_2(name:"jacky",gender:"male")

print(dog)

dog.name="재키"

print(dog)


//let 쓴 것은 안된다.. ex)dog.gender = "female"

//또한 구조체도 let으로 선언 하면 인스턴스를 바꾸는 것이 불가능하다.

class Cat{
    var name:String
    
    let gender:String
    
    init(name:String,gender:String)
    {
        self.name=name
        self.gender=gender
    }
}//클래스는 참조 타입이라서 let 으로 표현해도 괜찮다.. ->참조타입과 값타입의 차이

let cat=Cat(name:"yomi",gender: "male")
    
cat.name="gunter"

print(cat.name)

//cat.gender="female"

//print(cat.gender)

struct Stock{
    var averagePrice:Int
    var quantity:Int
    var purchasePrice:Int{
        get{
            return averagePrice*quantity
        }
        //만약 newPrice를 안적으면 newValue로 대신 적어도 된다.
        set(newPrice){
            averagePrice=newPrice/quantity
        }
    }
}

var stock = Stock(averagePrice: 2300, quantity: 3)

print(stock)

stock.purchasePrice

stock.purchasePrice=3000

stock.purchasePrice

stock.averagePrice

class Account{
    var credit:Int{
        //실행되기 직전
        willSet{
            print("잔액이 \(credit)원에서 \(newValue)원으로 변경될 예정입니다.")
        }
        
        //실행된 직후
        didSet{
            print("잔액이 \(oldValue)원에서 \(credit)원으로 변경되었습니다.")
        }
    }
    init(credit:Int){
        self.credit=credit
    }
}

var account=Account(credit:1000)

account.credit=2000

//타입 프로퍼티

struct SomeStructure{
    static var storedTypeProperty="Some value" // 스토어
    static var computedTypeProperty:Int{
        return 1
    }
}

SomeStructure.computedTypeProperty

SomeStructure.storedTypeProperty

SomeStructure.storedTypeProperty="hello"

SomeStructure.storedTypeProperty

/*
 클래스와 구조체의 공통/차이점
 공통점
 -값을 저장할 프로퍼티를 선언 할수 있다.
 -함수적 기능을 하는 메서드를 선언할 수 있다.
 -내부 값에 .을 사용하여 접근할 수 있다.
 -생성자를 사용해 초기 상태를 설정할 수 있다.
 -extension을 이용하여 기능을 확장할 수 있다.
 -Protocol을 채택하여 기능을 설정할 수 있다.
 
 차이점
클래스:
 -참조타입이다.
 -ARC로 메모리를 관리,상속이 가능,타입 캐스팅을 통해 런타임에서 클래스 인스턴스의 타입을 확인 할수 있다.
 -deinit을 사용하여 클래스 인스턴스의 메모리 할당을 해제할 수 있다.
 -같은 클래스 인스턴스를 여러개의 변수에 할당한 뒤 값을 변경 시키면 모든 변수에 영향을 줌(메모리가 복사됨)
 -힙영역과 관련이 있다.
 
 구조체
 -갑타입이다.
 -구조체 변술로 새로운 변수에 할당할 때마다 새로운 구조체가 할당 된다.
 -같은 구조체를 여러개의 변수에 할당한 뒤 값읋 변경시키더라도 다른변수에 영향을 주지않음(값 자체를 복사)
 -스택과 관련이 있다.
- */

class SomeClass{
    var count:Int=0
}

struct SomeStruct{
    var count:Int=0
}

var class1=SomeClass()
var class2=class1
var class3=class1

class3.count=2

class1.count

var struct1=SomeStruct()
var struct2=struct1
var struct3=struct1

struct2.count=1
struct3.count=2

struct1.count
struct2.count
struct3.count

//상속: 부모가 자식에게 재산을 물려주는 행위(클래스사이에 이루어 지는 것)

class Vehicle{
    //final은 재정의 불가능 ㅎ다.
    //final var currentSpeed=0.0
    var currentSpeed=0.0
    
    var description:String{
        return "traveling at \(currentSpeed) miles per hours"
    }
    
    func makeNoise(){
        print("speaker on")
    }
}

/*
 class 클래스 이름: 부모클래스 이름{
    //하위 클래스 정의
 }
 */

class Bicycle:Vehicle{
    var hasBasket = false
}

var bicycle = Bicycle()

bicycle.currentSpeed
bicycle.currentSpeed=15.0

bicycle.currentSpeed

//오버라이딩: 덮어 씌우기 -> 같은 기능인데 다르게 실행하기 위하여 사용하는 기법
//만약 덮어 씌운거를 안쓰고 싶으면 super을 사용하면 된다(중요)

class Train:Vehicle{
    override func makeNoise() {
        super.makeNoise()
        print("choo choo")
    }
}

let train = Train()

train.makeNoise()

class Car: Vehicle{
    var gear = 1
    
    override var description: String{
        return super.description + "in gear \(gear)"
    }
}

let car = Car()

car.currentSpeed = 30.0

car.gear = 2

print(car.description)

class AutomaticCar:Car{
    override var currentSpeed: Double{
        didSet{
            gear = Int(currentSpeed/10)+1
        }
    }
}

let automatic = AutomaticCar()

automatic.currentSpeed = 35.0

print("AutomaticCar: \(automatic.description)")

//타입 캐스팅
/*
 인스턴스의 타입을 확인하거나 어떠한 클래스의 인스턴스를 해당 클래스 계층구조의 슈퍼 클래스나 서브 클래스로 취급하는 방법 is,as를 이용하면 된다.
 */
class MedialItem{
    var name:String
    
    init(name:String)
    {
        self.name=name
    }
}

class Movie:MedialItem{
    var director:String
    
    init(name:String,director:String)
    {
        self.director=director
        super.init(name: name)
    }
}

class Song:MedialItem{
    var artist:String
    init(name:String,artist:String){
        self.artist=artist
        super.init(name:name)
    }
}

let library=[
    Movie(name:"기생충",director: "봉준호"),
    Song(name:"Butter",artist: "BTS"),
    Movie(name:"올드보이",director: "박찬욱"),
    Song(name:"Wonderwall",artist: "Oasis"),
    Song(name:"Rain",artist: "이적")
]

var movieCount = 0
var songCount = 0

for item in library{
    if item is Movie{
        movieCount += 1
    }else if item is Song{
        songCount += 1
    }
    
}

print("Media library contains \(movieCount) movies and \(songCount) songs")

//형변환 : 다운 캐스팅 이용

for item in library{
    
    if let movie = item as? Movie{
        print("Movie: \(movie.name),dir.\(movie.director)")
    }else if let song = item as? Song{
        print("Song: \(song.name),by \(song.artist)")
    }
}

//assert와 guard문

/*
 assert:특정 조건을 체크하고 ,조건이 성립 되지 않으면 메세지를 출력하게 할 수 있는 함수
 assert 함수는 디버깅 모드에서만 동작하고 주로 디버깅 중 조건의 검증을 위하여 사용한다.
 */

var value = 0
assert(value == 0)
/*
 value = 2
 assert(value==0,"값이 0이 아닙니다.")
 */

//guard: 무언가를 검사하여 그 다음에 오는 코드를 실행 할지 말지 결정하는 것(조건문의 일종)
/*
 guard문에 주어진 조건문이 거짓 일때 구문이 실행됨.
 guard 조건 else{
    //조건이 false 이면 else 구문이 실행 되고,
    return or throw or break를 통해 이 후 코드를 실행하지 않도록 한다.
 }
 */

func guardTest(value:Int?){
    guard let value = value else {return}
    print(value)
}

guardTest(value: 2)

guardTest(value: nil)

//프로토콜: 특정 역할을 하기 위한 메서드,프로퍼티,기타 요구사항드의 청사진

/*
 protocol 이름{
 
 }
 */

protocol SomeProtocol{
    
}

protocol SomeProtocol2{
    
}
/*
struct SomeStructure: SomeProtocol,SomeProtocol2{
    
}
*/

protocol FirstProtocol{
    var name:Int{get set} //읽기 쓰기 전용
    
    var age:Int{get}//읽기 전용
}

protocol AnotherProtocol{
    static var someTypeProperty:Int{get set}
}

protocol FullyNames{
    var fullName:String{get set}
    func proinFullName()
}

/*
 struct Person:FullyNames{
    var fullName:String
    func printFullName()
    {
        print(fullName)
    }
 }
 */

protocol SomeProtocol3{
    func someTypeMethod()
}


protocol SomeProtocol4{
    init(someParameter:Int)
}


protocol SomeProtocol5{
    init()
}


class SomeClass_2:SomeProtocol5{
    required init(){
    }
}

/*
 익스텐션:기존의 클래스,구조체,열거형,프로토콜에 새로운 기능을 추가하는 기능
 -연산타입프로퍼티/연산 인스턴스 프로퍼티
 -타입메서드,인스턴스 메서드
 -이니셜라이저
 -서브스크립트
 -중첩타입
 -특정 프로토콜을 준수할 수 있도록 기능추가
 -기존에 있던거 오버라이드는 불가능
 -연산프로퍼치 추가가능, 저장프로퍼티/프로퍼티 감시자 추가불가능
*/

 /*
  extension SomeType{
    //추가기능
  }
  */

extension Int{
    var isEven:Bool{
        return self%2==0
    }
    
    var isOdd:Bool{
        return self%2==1
    }
}

var number=3

number.isOdd

number.isEven

extension String{
    func convertToInt() ->Int?{
        return Int(self)
    }
}
var string_3 = "0"

string_3.convertToInt()

//열거형 : 연관성이 있는 값을 모아 놓은 것을 말한다.

enum CompassPoint:String{
    //다른 언어와 다르게 int형 말고 다른 것도 적을 수 있다.
    case north = "북"
    
    case south = "남"
    
    case east = "동"
    
    case west = "서"
    //한 줄로도 표현 가능
}

var direction=CompassPoint.east

direction = .west

switch direction{
case .north:
    print("north")
    print(direction.rawValue)
    
case .south:
    print("south")
    print(direction.rawValue)

case .east:
    print("east")
    print(direction.rawValue)
    
case .west:
    print("west")
    print(direction.rawValue)
}

let direction2 = CompassPoint(rawValue: "남" )

//연관 값을 갖는 법

enum PhoneError{
case unknown
case batteryLow(String)
}

let error = PhoneError.batteryLow("배터리가 곧 방전됩니다.")

switch error{
case .batteryLow(let message):
    print(message)
    
case .unknown:
    print("알수 없는 에러입니다.")
}


/*
 옵셔널 체이닝: 옵셔널에 속해 있는 값이 nil일지도 모르는 프로퍼티,메서드,서브스크립션 등을
            가져오거나 호출할 때 사용할 수 있는 일련의 과정
*/

struct Developer{
    let name:String
}

struct Company{
    let name:String
    var developer:Developer?
}

var developer = Developer(name:"han")

var company=Company(name:"jacky",developer: developer)

print(company.developer)

//print(company.developer.name)

print(company.developer?.name)

print(company.developer!.name)

/*
 try-catch:프로그램 내에서 에러가 발생한 상황에 대해 대응하고 이를 복구하는 과정
 발생-감지-전파-조작을 일급 클래스로 제공함
 */


enum PhoneError_2:Error{
    case unknown
    case batteryLow(batteryLevel:Int)
}

//throw PhoneError_2.batteryLow(batteryLevel:20)

func checkPhoneBatteryStatus(batteryLevel:Int)throws->String{
    guard batteryLevel != -1 else{throw PhoneError_2.unknown}
    guard batteryLevel > 20 else{throw
        
        PhoneError_2.batteryLow(batteryLevel:20)
        
    }
    return "배터리 상태가 정상입니다."
}


/*
 do {
    try 오류 발생 가능코드
 }catch 오류패턴{
 처리코드
 }
 */
do{
    try checkPhoneBatteryStatus(batteryLevel: 20)
}catch PhoneError_2.unknown{
    print("알 수 없는 에러입니다.")
}catch PhoneError_2.batteryLow(let batteryLevel){
    print("배터리 전원 부족, 남은 배터리 : \(batteryLevel)%")
}catch{
    print("그 외 오류 발생:\(error)")
}

let status = try? checkPhoneBatteryStatus(batteryLevel: -1)

print(status)

let status2 = try? checkPhoneBatteryStatus(batteryLevel: 25)

print(status2)

let status3 = try! checkPhoneBatteryStatus(batteryLevel: 30)

print(status3)

/*
 클로저란? 코드에서 전달 및 사용할 수 있는 독립 기능 블록이며, 일급 객체의 역할을 할 수있음.
 일급객체? 전달 인자로 보낼 수 있고, 변수/상수 등으로 저장하거나 전달할 수 있으며, 함수의 반환 값이 될 수도       있다.
 클로저 표현식 : 강의 30초 쯤 보면 된다.
 */

/*
 {(매개 변수) -> 리턴타입 in
    실행구문
 }
 */

let hello3 = {()->() in
    print("hello")
}

hello3()

let hello2 = {(name:String)->String in

return "Hello, \(name)"
}

//hello2(name:"jacky")

hello2("jacky")

func doSomeThing(closure:()->()){
    closure()
}

doSomeThing(closure: {()->() in
    print("hello")
})

doSomeThing() {
print("hello2")
}

doSomeThing {
print("hello3")
}

func doSomething2()->()->(){
    return { ()->() in
        print("hello4")
    }
}

doSomething2()()

func doSomething2(success:()->(),fail:()->()){
    
}
doSomething2()
/*
doSomething2{

} fail: {

<#code#>
}
*/

func doSomething3(closure:(Int,Int,Int)->Int){
closure(1,2,3)
}

doSomething3(closure: { (a,b,c) in
return a+b+c
})

doSomething3(closure: {
return $0+$1+$2
})

doSomething3(closure: {
$0+$1+$2
})

doSomething3() {
$0+$1+$2
}

doSomething3 {
$0+$1+$2
}

/*
 고차함수: 다른 함수를 전달 인자로 받거나 함수 실행의 결과를 함수로 반환하는 함수
 map,filter,reduce가 있다.
 */

//map

let numbers_2 = [0,1,2,3]

let mapArray = numbers_2.map{(number)->Int in
    return number*2
}
print("map(mapArray)")


//filter

let intArray=[10,5,20,13,4]

let filterArray = intArray.filter{$0 > 5}

print("filter \(filterArray)")

//reduce

let someArray = [1,2,3,4,5]

let reduceResult = someArray.reduce(0){
    (result: Int,element:Int)->Int in
    print("\(result) + \(element)")
    return result+element
}

print("reduce \(reduceResult)")
