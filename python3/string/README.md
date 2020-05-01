# 문자열

## 빈 문자열을 선언하고 더하기 연산으로 이어 붙이기 가능
~~~python
string = ""

string += "abc"
string += "def"

print(string) # "abcdef"
~~~

## 문자열은 immutable(변하지 않음)한 변수!
~~~python
string = "Hello World"
string[3] = "2" # ERROR!!!!!!
~~~

## 문자열도 내부는 리스트로 구현되어 있음.
* in 사용 가능
~~~python
>>> "e" in "blueberry"
True
~~~
* 문자열도 in 사용 가능
~~~python
>>> "blue" in "blueberry"
True
~~~

## lower upper title
* lower() --> 문자열 소문자로 변경
* upper() --> 문자열 대문자로 변경
* title() --> 단어의 시작만 대문자 나머지는 소문자로 변경

## spiit()
* 문자열을 여러개로 쪼개는 함수
* 매개변수의 기본 값은 공백 --> 매개변수를 안넣으면 공백으로 문자들이 짤림
* 매개변수가 문자 거나 문자열일 수도 있음.
~~~python
>>> "Hello World".split()
['HEllo', 'World']
>>> "abaaabaabaaabbbaabbababbbaaaabababaaabaa".split('a')
['', 'b', '', '', 'b', '', 'b', '', '', 'bbb', '', 'bb', 'b', 'bbb', '', '', '', 'b', 'b', 'b', '', '', 'b', '', '']
>>> "abaaabaabaaabbbaabbababbbaaaabababaaabaa".split('ab')
['', 'aa', 'a', 'aa', 'bba', 'b', '', 'bbaaa', '', '', 'aa', 'aa']
~~~

## join()
~~~python
>>> ' '.join(["Hello", "My", "Name", "is", "steven"])
'Hello My Name is steven'

>>> ''.join(["Hello", "My", "Name", "is", "steven"])
'HelloMyNameissteven'


~~~

