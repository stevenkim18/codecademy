# 모듈

## datetime
* 파이썬에서 시간을 사용할 수 있는 모듈

### import 하기
~~~python
from datetime import datetime
~~~

### 현재 시간 불러오기
~~~python
>>> datetime.now()
datetime.datetime(2020, 5, 4, 10, 52, 36, 541385)
~~~

### 시간 저장하기
* datetime(년, 월, 일, 시, 분, 초, 나노초) 로 저장 가능
~~~python
>>> birthday = datetime(1993, 1, 18, 8, 00, 23)
>>> birthday
datetime.datetime(1993, 1, 18, 8, 0, 23)
~~~

### 저장된 시간 출력하기
* 객체에 변수로 저장되어 있음.
~~~python
>>> birthday.year
1993
>>> birthday.day
18
>>> birthday.month
1
>>> birthday.hour
8
>>> birthday.second
23
~~~

