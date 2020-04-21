# 리스트
## 리스트에 다양한 값 가능
~~~python
ints_and_strings = [1, 2, 3, 'four', 'five', "HelloWorld!"]
~~~

## 리스트 안에 리스트 가능
~~~python
heights = [['Jenny', 61], ['Alexus', 70], ['Sam', 67], ['Grace', 64], ['Vik', 68]]
~~~

## zip을 사용해서 두 리스트 합치기
~~~python
names = ['Jenny', 'Alexus', 'Sam', 'Grace']
dogs_names = ['Elphonse', 'Dr. Doggy DDS', 'Carter', 'Ralph']

names_and_dogs_names = zip(names, dogs_names)
#[('Jenny', 'Elphonse'), ('Alexus', 'Dr. Doggy DDS'), ('Sam', 'Carter'), ('Grace', 'Ralph')]
~~~

## 리스트의 값 추가하기
~~~python
my_list = [1, 2, 3]
my_list + 4 # --> 애러
my_list + [4] # [1, 2, 3, 4]
~~~

## range
* range(정수)를 하면 0 부터 정수 전까지 수를 리스트에 저장
~~~python
my_range = range(10)
print(list(my_range)) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
~~~
* range(시작수, 끝수, 간격)
~~~python
list1 = range(5, 15, 3) # [5, 8, 11, 14]
~~~
