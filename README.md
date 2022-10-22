# TIL
Today I Learn

- from 2022.10.20 ~ start


2022.10.22 (sat)

## *파이썬 프로그래밍의 기초, 자료형

자료에 대한 타입 : 숫자, 문자열, 불린(참/거짓)

어떤 값을 담는 자료구조 : 변수, 리스트, 튜플, 딕셔너리, 집합

변수 : a = a + 1 
: 오른쪽에 있는 값을 왼쪽 상자에 넣는다. -> a라는 상자에 a+1을 넣는다.

1. 숫자형 
- 정수형 (1,2,-2) : int
- 실수 (1.25, 2.3) : float

타입 찍기 : print(type(변수명))

파이썬에서 
곱하기 *  나누기 / (자바에선 몫 구하는표현) 
파이썬에서 몫을 구하려면 // 사용 ex) a//b , 나머지를 구하려면 % 
제곱은 ** ex) a ** b 

2. 문자열 자료형 str (String의 약자)
1. “ “  큰 따옴표 ex) “Hello”
2. ‘ ‘ 작은 따옴표 ex) ‘hello‘
3. “”” “”” 큰 따옴표 *3 ex) “””Life is too short, You need python“””  
4.’’’ ‘’’ 작은 따옴표 *3 ex) ‘’’Life is too short, You need python’’’

- 문자열에 따옴표 포함시키기
ex) a = ‘python’s favorite food is perl’ 하고 실행하면 오류! ‘python’만 문자로 인식..
\’ 라고 써서 ‘는 문자야 라고 알려주어라 

- 여러 줄로 이루어진 문자열
이스케이프 코드 : \n 으로 문장띄기 가능. \t 은 문자열 사이에 탭 간격을 줄 때 사용
“”” 문자문자문자 “”” 를 쓰면 이스케이프 코드를 쓰지 않아도 여러줄 문장 쓰기 좋다.
문자열을 더하면? 문자가 서로 붙는다. 문자열 * 숫자를 하면 문자열을 숫자만큼 반복하여 print 가능

- 인덱싱(Indexing) : 다른 언어에는 문자열에 인덱싱이 없다. 파이썬엔 있음
 a = “Life is too short”
print(a[5]) 하면 결과 i가 나옴, -1하면 t가 나옴 -> 거꾸로

-슬라이싱(slicing) : 문자열을 자른다.
a[~이상: ~미만: 간격]  비워놓으면 무조건 처음부터 시작함

ex) a = “20010331Rainy”
pinrt(a[:8]) 를 출력하면 20010331 이 나옴 즉 첫 글자부터 시작해서 8번 인덱스 전까지 출력



-문자열 포매팅
ex) a = “ I eat %d apples. “ % 3
print(a) 라고하면 결과값으로 I eat 3 apples 라고 나온다.
%d를 사용하지 않으면 b = “I eat ” + str(3) + “ apples”라고 사용하여야 함

이를 활용하여 
number = 10
day = “three”
a = “I ate %d apples. so I was sick for %s days.” % (number, day)
print(a)로 가능 (각각 rappring) 

이것도 가능 : 변수에 맞게 포매팅 가능
ex1) “그녀는 {age} 이고 이름은 {name}이다.”.format(name=”이시영”, age = 25)
ex2) name = “강하나”
     a = f”나의 이름은 {name}입니다.” => 앞에 f 하나만 넣어도 ok

-정렬과 공백 (잘 안쓰임)
 a = “%10s” % “hi” 하고 프린트하면           hi 라고 나옴 -10으로 하면 왼쪽 정렬
 
 -소수점 몇 번째 자리까지 나타내겠다.
 a = “%0.4f” % 3.42134234 에서 0.4의 의미는 0은 간격, 4는 소수점 남기는 자리 수
=> 3.4213 라는 결과가 나옴

-문자열 개수 세기(count)
a = “hobby”
print(a.count(‘b)) 하면 2 

- 위치 알려주기 1 (find)---> 더 많이 사용
 print(a.find(‘b)) 하면 2가 나옴 인덱스가 0부터 시작해서 2번째에 있다! (처음에 걸리는 b), 없으면 -1 나옴

- 위치 알려주기 2(index)

- 문자열 삽입(join)
a = “,”.join(“abcd”) ->.join() 사용하면 => a,b,c,d 라고 나옴
a = “,”.join([“a”,”b”,”c”]) => 하면 a,b,c 나옴 (리스트랑 많이 사용)

-소문자를 대문자로 바꾸기(upper) <-> lower

-공백없애기(strip)

-문자열 바꾸기(replace)
 a= “Life is too short”
print(a.replace(“Life”, “Your leg”)) 라고하면 Your leg is too short라고 결과 나옴

-문자열 나누기(split) -> 많이 사용!!
a = “Life is too short”
print(a.split()) 하면 띄어쓰기를 기준으로 리스트를 만듬 => [‘Life’,’is’,’too’,’short’]
a = “a:b:c:d”일때
print(a.split(“:”) 하면 :을 기준으로 자름 

