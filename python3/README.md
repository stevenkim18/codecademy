* string은 '' "" 둘다 지원
* 정수 int, 실수 float
~~~
2 ** 2 --> 2 제곱 / 4 ** 0.5 --> 4의 1/2제곱 
~~~

### 문자열 합치기
~~~python
str = "Hello" + "World" 가능
~~~

### 여러줄 문자열 저장하기
~~~python
str = ''' 
Hello
World
'''
~~~

### 함수 만들기
~~~python
# 함수명 뒤에 괄호 넣어줘야 함!
def say_hello(): 
  print("hello")
~~~

### 키워드 매개변수
* 함수를 호출할 때 매개변수의 이름에 직접 값을 넣을 수 있음.
~~~python
def sum(a, b):
  return a + b
  
sum(b = 10, a = 12) # 직접 매개변수 이름을 불러서 대입 가능

# 함수 생성시 매개변수를 기본 값으로 넣어 둘 수도 있음
def greeting(name, words="Hello")
  print(words + name)
~~~

## 함수에서 여러개의 리턴 값을 줄 수 있음.
~~~python
def get_boundaries(target, margin):
  low_limit = target - margin
  high_limit = margin + target
  return (low_limit, high_limit)

low ,high = get_boundaries(100, 20)
~~~

## 변수의 타입 확인하기
~~~python
print(type(변수)) # class 'str'
~~~

## try execption
~~~python
def divides(a,b):
  try:
    result = a / b
    print (result)
  except ZeroDivisionError:
    print ("Can't divide by zero!")
~~~

## 리스트
* 한 리스트에 다양한 타입의 변수 저장 가능
* 리스트 안에 리스트도 저장 가능
~~~python
jenny = ['Jenny', 61, 10.5]
heights = [['Jenny', 61], ['Alexus', 70], ['Sam', 67], ['Grace', 64]]
~~~

## zips
* 
