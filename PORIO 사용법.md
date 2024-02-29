# porio란?
초보자들이 간단하게 코딩할수있게 만드는 단순 인터프린터 언어입니다.

# porio 사용법
## 1. 출력
porio에는 아쉽게도 입력이 없습니다.
하지만 다음과 같이 출력 할수 있습니다.
이 코드는 porio에서의 출력입니다.
```porio
valLog("Hello")
```
## 2. 변수
porio 에서는 변수 선언도 가능합니다.

네 종류의 타입이 있는데요
```
integer
string
bool
float
```
입니다.
변수 선언부터 해볼까요?
변수는 다음과 같이 선언됩니다.
```porio
val (변수타입) (변수이름)
```

이제 선언을 했으니 끝인가요?
아닙니다. 변수 정의를 해야죠.
porio에서는 변수 정의를 다음과 같이 합니다.
```
assign (변수이름) "값"
```
아무리 정수나 실수, bool이라도 무조건 "값" 안에 들어가야합니다.
```
assign test "321"
```
처럼요.

이제 변수 정의를 했으니 변수를 써먹어야겠죠?
아쉽게도 porio 에서는 연산자 (사칙,논리,등등)이 없습니다.
valLog를 사용하시면 변수를 출력할수있습니다.

예제로 270031를 출력하는 방법을 알려드리겠습니다.

```
val integer test
assign test "270031"
valLog(test)
```
를 할시 270031이 출력됩니다.

## 3. 에러
porio에서의 에러는 다음과 같습니다.
```
LogError
```
명심하세요.
porio에서는 LogError밖에 없습니다.

## 4. 리스트
기초 리스트를 배워볼껍니다.

먼저 리스트를 선언해봅시다

```
val list (리스트 이름)
```
로 선언가능합니다.
두번째로 list를 조작해봅시다.
list 조작하는법은 다음과 같습니다

크게 두가지인

listAdd
listRemove
이 있습니다
예제를 보여드리겠습니다.
```
val list numbers
listAdd(numbers,"1")
listAdd(numbers,"2")
listAdd(numbers,"3")
listLog(numbers) 
```

이때 출력창엔 아마도
출력: [1, 2, 3]
이 나올것입니다.
remove도 해봐야죠. 
```
val list numbers
listAdd(numbers,"1")
listRemove(numbers,"1")
listAdd(numbers,"3")
listLog(numbers)
```

이러면 출력엔 [3]
만 나올것입니다.

그외에도 map,dictionary,set이 있다만, 일단 나중에 알아봅시다.

## 5. 문자열 조작

기본적으로 1개만 알아보겠습니다.

replace()는 문자열 대체 조작이라고 볼수있습니다.
한번 replace 예시 나랭 코드를 보여드리겠습니다.
```
val string myString
assign myString "Hello,NaLang!"
replace(myString,"NaLang","World")
valLog(myString)
```
예시 코드를 설명해 드리자면, myString은
"Hello,NaLang!"으로 설명 되었지만
replace로 NaLang을 World로 바꾸는 코드입니다.

그외는 인터프린터 코드 뜯어가서 분석해주세요.

## 6. loop

porio에서는 while,if,for이랑 사칙연산, 심지어 함수같은 기초도 없습니다.
다만 한가지 있긴하죠 loop 입니다!
porio의 loop 구문은 다음과 같은 형식을 가집니다:
```
loop <반복 횟수>
  <반복될 코드 블록>
endloop
```

예시로 loop로 Hello를 10번 출력해볼까요?
```
loop 3
  val string message
  assign message "Hello"
  valLog(message)
```

# 끝
끝입니다 감사합니다
