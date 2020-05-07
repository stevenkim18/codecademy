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
