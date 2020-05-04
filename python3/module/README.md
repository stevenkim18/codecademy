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

### 날짜 빼기
~~~python
>>> datetime(2019, 1, 1) - datetime(2018, 1, 1)
datetime.timedelta(days=365)

>>> datetime.now() - datetime(2020, 1, 1)
datetime.timedelta(days=124, seconds=40168, microseconds=549700)
~~~

### 문자열에서 datetime 형식으로 바꾸기
* datetime 전용 서식 지정자를 통해 문자열로 되어있는 날짜와 시간을 datetime 객체로 변환 가능(서식지정자는 검색 ㄱㄱ)
~~~python
>>> parsed_date = datetime.strptime('Jan 18, 1993', '%b %d, %Y')
>>> parsed_date
datetime.datetime(1993, 1, 18, 0, 0)

>>> parsed_date.year
1993

>>> parsed_date.month
1
~~~

### datetime에서 문자열로 바꾸기
~~~python
>>> date_string = datetime.strftime(datetime.now(), '%b %d, %Y')
>>> date_string
'May 04, 2020'
~~~

