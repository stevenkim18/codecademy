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
9
~~~
* new.txt
~~~
> cat new.txt
newfile!!%
~~~

## 파일에 추가하기
* "a" --> append mode
~~~python
>>> with open("new.txt", "a") as file:
...     file.write("append")
...
6
~~~
* new.txt
~~~
> cat new.txt
newfile!!append%
~~~

## with을 사용하는 이유
* 원래 사용 방식 open() --> close()
~~~python
file = open("new.txt", "a")
file.write("Hello")
file.close()
~~~
* 그런게 보통 close를 잘 까먹고 안해줌. close를 안해주면 메모리 영역으로 잡혀 있음.
* with 안에서 해결하는 것이 편함.
#### 참고
https://devpouch.tistory.com/79

## csv 파일 읽고 쓰기

### csv 파일 이란
* csv 파일은 Comma-Separated Values 즉 콤마로 분류 되어 있는 값들이란 뜻
* 쉼표로 데이터가 분류되어 있음.
~~~
Name,Username,Email
steven,1188ss,111888@navar.com
hannh,gogoh12,hahw@hanmail.com
john,j1122wq,john@goggle.com
song,ss231s,song11@gooogle.com
~~~

### csv 모듈 사용하기
~~~python
import csv
~~~

~~~python
>>> import csv

>>> with open("info.csv", newline="") as file:
...     reader = csv.Di
...     reader = csv.DictReader(file)
...     for row in reader:
...             print(row)
...
OrderedDict([('Name', 'steven'), ('Username', '1188ss'), ('Email', '111888@navar.com')])
OrderedDict([('Name', 'hannh'), ('Username', 'gogoh12'), ('Email', 'hahw@hanmail.com')])
OrderedDict([('Name', 'john'), ('Username', 'j1122wq'), ('Email', 'john@goggle.com')])
OrderedDict([('Name', 'song'), ('Username', 'ss231s'), ('Email', 'song11@gooogle.com')])
~~~


