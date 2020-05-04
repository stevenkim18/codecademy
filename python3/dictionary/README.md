# 딕셔너리

## 딕셔너리는 key : value 형식
* value로는 어떤 자료형이든 올 수 있음.
* key로는 리스트나 튜플 딕셔너리는 사용 불가!

## 딕셔너리에 새로운 key value 추가하기
~~~python
>>> dict = {"name": "steven", "age": 29}

>>> dict
{'name': 'steven', 'age': 29}
>>> dict["address"] = "anyang"

>>> dict
{'name': 'steven', 'age': 29, 'address': 'anyang'}
~~~
* 기존에 있는 key를 사용하면 값이 변경됨.
~~~python
>>> dict
{'name': 'steven', 'age': 29, 'address': 'anyang'}

>>> dict["name"] = "Steven Kim"

>>> dict
{'name': 'Steven Kim', 'age': 29, 'address': 'anyang'}
~~~

## 여러개 key 추가 하기(update 함수 사용)
~~~python
>>> dict
{'name': 'Steven Kim', 'age': 29, 'address': 'anyang'}

>>> dict.update({"tall": 184, "major": "accounting"})

>>> dict
{'name': 'Steven Kim', 'age': 29, 'address': 'anyang', 'tall': 184, 'major': 'accounting'}
~~~

## List Comprehensions 사용해서 딕셔너리 만들기
~~~python
>>> lan = ["Java", "Python", "Ruby"]

>>> framework = ["Spring", "Django", "Rails"]

>>> stack = {key:value for key, value in zip(lan, framework)}

>>> stack
{'Java': 'Spring', 'Python': 'Django', 'Ruby': 'Rails'}
~~~
