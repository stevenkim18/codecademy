# 파일

## 파일 열기
* with 와 open을 사용해서 파일 열기
* as 뒤에 변수를 사용해서 파일 객체 변수로 저장
~~~python
with open("text.txt") as file:
~~~

## 파일 읽기
* read()함수로 파일 읽기
* text.txt
~~~
HelloWorld!!
123
456

789
~~~
~~~python
>>> with open("text.txt") as file:
...     print(file.read())
...
HelloWorld!!
123
456

789
~~~

## 파일 한줄씩 모든 줄 읽어오기
* readlines() 사용
* 리스트로 저장됨.
~~~python
>>> with open("text.txt") as file:
...     print(file.readlines())
...
['HelloWorld!!\n', '123\n', '456\n', '\n', '789\n']
~~~

## 파일 한줄 만 읽어오기
* readline() 사용
~~~python
>>> with open("text.txt") as file:
...     print(file.readline())
...
HelloWorld!!

>>> with open("text.txt") as file:
...     print(file.readline())
...     print(file.readline())
...
HelloWorld!!

123
~~~

## 파일에 쓰기
* open(파일 이름, 모드)
* 읽기 모드 --> "r" 쓰기 모드 --> "w"
~~~python
>>> with open("new.txt", "w") as file:
...     file.write("newfile!!")
...
~~~
* new.txt
~~~
> cat new.txt
newfile!!%
~~~
