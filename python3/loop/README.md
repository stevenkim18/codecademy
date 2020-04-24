# 반복문
## 파이썬에서 반복문과 리스트를 떌 수 없는 사이
~~~python
names = ["Steven", "Hannah"]
fot name in names:
  print(name)
# Steven
# Hannah
~~~

## range로 for문 생성 가능
~~~python
promise = "I will not chew gum in class"

for i in range(5):
  print(promise)

# "I will not chew gum in class" 5번 출력
~~~

## continue
* continue를 사용하면 반복문 아래 있는 명령어 무시하고 위에 부터 다시 실행
~~~python
big_number_list = [1, 2, -1, 4, -5, 5, 2, -9]

for i in big_number_list:
  if i < 0:
    continue
  print(i)
~~~

## 리스트 이용하기
* 한줄로 리스트에 들어갈 값을 for문과 조건문으로 표현 가능
~~~python
heights = [161, 164, 156, 144, 158, 170, 163, 163, 157]

can_ride_coaster = [height for height in heights if height > 161]
# [164, 170, 163, 163]
~~~
* 리스트 원소들에 변형도 가능
~~~python
my_upvotes = [192, 34, 22, 175, 75, 101, 97]

updated_upvotes = [vote_value + 100 for vote_value in my_upvotes]
~~~
~~~python
celsius = [0, 10, 15, 32, -5, 27, 3]

fahrenheit = [(c * 9/5 + 32) for c in celsius]
~~~

## for문에서 여러개의 변수 사용하기
* 리스트 안에 리스트 같은 경우에 사용 가능
~~~python
for i, j in [(1, 2), (9, 3), (5, 7)]
  sum1 += i # 1, 9, 5
  sum2 += j # 2, 3, 7
~~~
