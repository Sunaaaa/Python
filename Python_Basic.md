

# 용어 정리 

## Data 

- 일반적으로 측정이나 관찰을 통해서 모아 놓은 값의 집합
- 사실을 표현하는 하나의 단면일 뿐, 데이터 자체의 의미는 없다.

## Data 분석(Data Analysis)

- Data를 기반으로 의미있는 사실/내용을 끌어내는 작업
- Data의 양이 많으면 많을 수록 분석을 통해 도출할 수 있는 내용이 풍부하다. 

## 빅 데이터(Big Data)

- 일반적인 의미 : 기존의 관리 체계/방법 또는 분석 체계/방법으로는 감당할 수 없는 많은 양의 데이터를 의미한다. 

## 빅 데이터의 3가지 특징(3V)

1. Volume 
   - 데이터의 규모 : 데이터의 규모가 기존의 데이터의 규모보다 확연히 커야한다. 
     - 규모 : GB -> TB -> PB -> EB -> ZB -> YB
2. Variety
   - 데이터의 다양성
     - 여러개의 다양한 데이터 형식
     - 데이터가 비정형화된 형식으로 구성이 되어 있다. 
3. Velocity 
   - 데이터의 발생 속도 
     - 데이터가 실시간 적으로 발생된다. 
     - 데이터는 지속적으로, 끊임없이 생성되어 계속 쌓인다.

## 빅 데이터 분석 방법

1. EDA (Exploratory Data Analysis)
   - 탐색적 데이터 분석
   - 일반적인 수학 식을 이용해서 빅데이터를 분석한다.
     - A 학교의 전체 수학 평균, 분산 등을 분석하여 해당 학교의 수학 실력을 도출한다. 
2. 통계적 가설 검정
   - 통계를 기반으로 빅데이터를 분석한다.
   - 여론조사 등 99.9%의 확률 
3. Machine Learning
   - 많은 양의 데이터를 기반으로 컴퓨터에게 프로그램을 학습시켜 학습된 내용을 근간으로 분석한다.
4. Deep Learning

# Python

- 장점 
  - 데이터 분석에 탁월하고 최적화 되어 있다. 
  - 문자, 숫자 등의 데이터를 handlling하는데 최적이다.
  - 타 언어에 비해 상대적으로 배우기가 쉽다. 
  - 조각 단위로 실행이 가능하여, Interactive한 개발이 용이하고 개발자와의 communication이 좋다. 
  - Numpy, Pandas 등의 아주 강력한 라이브러리를 무료로 제공한다.
- 단점
  - 버전의 호환성이 없다. 
    - 2.x 버전과 3.x 버전의 호환성이 없다.

## 주석 

- #: 한줄 주석
- '''    ''' / """   """   : 여러줄 주석 (single quotation/double quotation)
- Ctrl + /  : 드래그한 영역만큼 한번에 # 주석 ( 빈 줄을 주석 처리 되지 않음 )

## 세미콜론 

- statement 가 끝날 때마다 뒤에 세미콜론(;) 를 붙이는 Java와는 달리 Python에서는 세미콜론(;)을 전혀 붙이지 않는다. 

## 변수 선언 

- 데이터 타입이 유연하게 사용되는 Weak Type의 언어
- 변수 선언 시, 데이터의 타입을 명시하지 않음 
- 어떤 데이터 타입이든 바인딩 할 수 있다. 

## 코드 실행

- Ctrl + Enter
- 코드가 몇번째 실행되었는지 알 수 있음

![1561700396474](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561700396474.png)

- 셀 =  edit mode

![1561701871662](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561701871662.png)

- 셀 밖을 누르고 b를 하면 아래에 새로운 셀이 생김

  ![1561701906549](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561701906549.png)

  - dd를 누르면 해당 셀을 지울 수 있음
  - z 키로 undo를 수행한다.

  

## 내장상수 

1. True : 참

2. False : 거짓

3. None

   - 값이 존재하지 않는다.
   - 해당 변수 안에 값이 없는다.
   - 해당 파라미터의 값이 없는다.
   
   ![1561707741813](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561707741813.png)

## 내장형 데이터 타입(Built - in Data Type)

- 이미 Python에 내장되어 있는 데이터 타입

### 숫자형 (Numeric Type)

- int, double 등의 숫자형 type을 명시했던 Java와 달리, Python에서는 별도의 숫자형 type을 명시하지 않아도 자동으로 해당 타입으로 바인딩되고 인식한다. 

- 정수와 실수의 구분이 없다.

  - a= 123	=> 정수

  - b= 3.1415926535	=> 실수

  - c= 3.14E10	=> 실수 (지수 형태로 표현, c = 3.14* 10의 10승)

    

    ### 연산 

    - div = 3/4	=> 결과값은 실수

      - 정수와 정수 연산의 결과값이 정수인 Java와 달리, Python에서는 연산의 결과값을 실수로 출력한다. (Python 3.x 버전 부터는 정수-정수의 연산의 결과 값이 실수로 출력된다.)

        ![1561708168732](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561708168732.png)

    - result = 3 ** 4	=> 3의 4제곱(3 * 3 * 3 * 3 = 81)

    - result = 10 % 3 	=> 나머지 연산

    - result = 10 // 3	=> 나눗셈의 몫 구하기

      ![1561708654342](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561708654342.png)

### str (Text Sequence Type, 순서가 있는 문자열 타입)

#### 문자열 생성 방법

- Java : 문자열(String)은 " "으로 표현하고, 문자(Char)은 ' '으로 문자열을 생성한다. 

- Python

  - 문자열과 문자의 구분이 없이, " " 또는 ' '으로 문자열을 생성한다. 

  - 둘 다 str이라는 Text Sequence Type이다. 

  - 여러 줄에 걸친 문자열도 생성할 수 있다. (문자열 자체에 개행('\n')이 포함)

    ![1561708999806](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561708999806.png)

#### 문자열 연산

- 문자열 + 문자열

  - 문자열을 연결 할 수 있다. 

  - first = '이것은 ', second = '소리 없는 ', third = '아우성'

    ![1561709243997](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561709243997.png)

- 문자열 + 숫자형 타입

  - 숫자형을 문자열로 자동으로 타입 변환하여 연산을 수행하는 Java와 달리, Python은 숫자형의 타입을 문자열로 임의로 바꿔주어야한다. 이 때, **<u>str() 함수</u>**를 사용한다.

    - 타입 변환 없이 연산 수행

      ![1561709465895](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561709465895.png)

    - str()을 통해 임의의 타입 변환 후 연산 수행

      ![1561709576252](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561709576252.png)

- 문자열 반복 연산

  - ***** 를 사용하여 문자열을 반복해서 여러 번 출력한다. (띄어쓰기 없음)

    ![1561709704541](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561709704541.png)

  - 문자열 뒤에 ' '를 추가하여 띄어쓰기의 효과를 준다.

    ![1561709741892](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561709741892.png)

#### 문자열 인덱싱(Indexing)

- str은 Text Sequence Type으로 순서가 있는 글자들의 모임이다. 그래서 문자열 자체를 배열처럼 사용할 수 있다.

- Python에는 배열이 존재하지 않기 때문에 배열 처럼 인덱스를 이용한 Indexing을 한다. (인덱스는 0부터 시작)

  - [0] : 첫번째 문자열
  - [-1] : 뒤에서 첫번째 문자열
  - [-2] : 뒤에서 두번째 문자열
  - 앞에서 부터 인덱싱 : 0,1,2,3,4....
    - 뒤에서 부터 인덱싱 : -1, -2, -3 ...
  
  ![1561709903363](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561709903363.png)

#### 문자열 슬라이싱(Slicing)

- 문자열의 원하는 부분만 뽑는다.

- 영역을 부여해서 해당 영역만큼의 문자열을 복사한다.

- [ : ] : ' : '를 기준으로 왼쪽은 inclusive(포함)이고, 오른쪽은 exclusive(불포함)이다. 

  - text[1:3] : text의 1,2번 인덱스만 뽑는다.

  - text[:3] : text의 처음부터 3번 인덱스 전까지만 뽑는다. (1,2번 인덱스만 뽑는다.)

  - text[3:] : text의 3번 인덱스부터 끝까지 뽑는다. 

  - text[:] : text의 처음부터 끝까지, 문자열 전체를 뽑는다.

    ![1561710273933](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561710273933.png)
    
  - text[: : -1] : text의 끝부터 처음까지 역순으로 뽑는다.
  
    ![1561975828604](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561975828604.png)

#### 문자열 in / not in

- 문자열 내에 특정 문자열이 있는지 없는지를 확인한다. 

- 결과는 True 또는 False

- 대소문자 구별

- ( '  ' **in**  '  ' ) : in을 기준으로  왼쪽의 문자열이 오른쪽의 문자열에 있으면 True, 아니면 False

- ( '  ' **not in**  '  ' ) : in을 기준으로  왼쪽의 문자열이 오른쪽의 문자열에 있으면 False, 아니면 True

- 오른쪽의 문자열에는 ' '으로 직접 문자열을 지정할 수 있고, 문자열이 바인딩된 변수를 지정할 수 있다.

  ![1561710705871](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561710705871.png)

#### 문자열 Formatting

- C언어의 prinf('  ', %d)와 같은 효과를 얻을 수 있다. 

- text = "사과 %d개" 라고 선언한 변수 뒤에 '%3' 을 추가하여 숫자로 값을 표현한다. 

  ![1561710841171](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561710841171.png)

- text = "사과 %d개" 라고 선언한 변수 뒤에 '%apple' 을 추가하여 숫자로 바인딩된 변수로 값을 표현한다. 

  ![1561710895254](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561710895254.png)

- text = "사과 %d개, 바나나 %s"라고 선언한 변수 뒤에 숫자와 숫자로 바인딩된 변수를 동시에 사용하여 값을 표현한다.

  ![1561710963774](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561710963774.png)
  
- text = "{ }" 라고 선언된 변수에 .format()을 사용한다. format()의 인자로는 문자열과 숫자 모두 가능하다.

  ![1561976038427](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561976038427.png)

- text="{}, {}"라고 선언된 변수에 .format()을 사용한다. format()의 인자로는 문자열과 숫자 모두 가능하다. 

  - 여러 개의 값을 Mapping할 때 필요하다. 

  - 인자의 개수만큼 인덱스를 붙여 사용할 수 있다. (인덱스는 0부터 시작한다.)

    ![1561976286953](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561976286953.png)

  - 만약, 인덱스를 바꿔서 실행할 경우, 주어진 인덱스의 값이 Mapping된다. 

    ![1561976420730](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561976420730.png)

#### 문자열 내장 함수

##### len() 

- 문자열의 길이를 구하는 함수 

- 집합 계열의 자료형의 크기를 구할 수 있다.

- Python이 가지는 내장함수 이므로 인자값으로 문자열을 받는다.

  ![1561711114916](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561711114916.png)

##### count()

- 문자열 내의 특정 문자열의 개수를 구하는 함수

- str 객체의 method 이므로 문자열의 method 형태로 호출한다. 

  ![1561711223156](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561711223156.png)

##### find()

- 문자열 내의 특정 문자열이 처음 나오는 인덱스를 반환하는 함수

- 만약, 특정 문자열이 문자열 내에 없으면 -1을 반환한다. 

- str 객체의 method 이므로 문자열의 method 형태로 호출한다. 

  ![1561711341597](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561711341597.png)

##### join()

- 문자열 사이에 특정 문자열을 삽입하는 함수

- str 객체의 method 이므로 문자열의 method 형태로 호출한다. 

  ![1561711413453](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561711413453.png)
  
- 문자열 '1234' 를 숫자로 바꿀 때, **<u>''.join('1234')</u>**

##### lower()

- 문자열을 소문자로 변환하는 함수 
- str 객체의 method 이므로 문자열의 method 형태로 호출한다.

##### upper()

- 문자열을 대문자로 변환하는 함수 
- str 객체의 method 이므로 문자열의 method 형태로 호출한다.

##### strip()

- 문자열의 앞 뒤 공백제거 
- str 객체의 method 이므로 문자열의 method 형태로 호출한다.

![1561711569645](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561711569645.png)

##### format()

- 문자열의 출력 형식을 설정한다. 
- str 객체의 method 이므로 문자열의 method 형태로 호출한다.



## Python Sequence Type : List

- Java의 ArrayList와 상당히 유사하다.
- Python에서는 배열이 존재하지 않기 때문에 List를 배열처럼 사용하면 된다.

#### List의 생성

- 공백 리스트 생성

  - list() 함수 사용 

    - a = list()

  - 대괄호 사용

    - a = [ ]

    ![1561977019440](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561977019440.png)

- 리스트 생성

  - a = [1,2,3]

    ![1561976942320](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561976942320.png)

  - 배열이 아닌 List 이기 때문에 다양한 타입의 데이터들이 들어올 수 있다. 

    ![1561977098016](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561977098016.png)

  - List 안의 List 생성도 가능하다.

    ![1561977156968](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561977156968.png)

#### List 인덱싱 (Indexing)

- 가장 앞의 요소 부터 인덱스 0을 갖는다.

- List 안의 List의 요소는 2차원 배열처럼 접근한다.

  ![1561977357944](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561977357944.png)

#### List 슬라이싱 (Slicing)

- List 슬라이싱의 결과는 List

- 주어진 영역 내의 List를 복사한다. 

  ![1561977500759](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561977500759.png)





#### List의 값 변경 시, 인덱싱과 슬라이싱의 차이 

- 인덱싱 (Indexing) 을 통한  List 값 변경

  - 해당 요소의 값을 List 또는 주어진 값으로 변경
  - 추가한 리스트가 해당 요소로 추가되어, 인덱스가 늘어나거나 줄어들지 않는다.

  ![1561977903720](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561977903720.png)

- 슬라이싱 (Slicing) 을 통한 List 값 변경

  - 슬라이싱을 통해 복사된 영역에 주어진 리스트를 대체한다.

  - 주어진 리스트가 대체되어 삽입되기 때문에, 인덱스가 늘어나거나 줄어들 수 있다.

    ![1561978278577](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561978278577.png)

- 예제 ) a = [1,2,3,4,5,6,7] 을 a = [1,2,6,7]로 변형해보자

  - 2번 인덱스부터 4번 인덱스까지 공백 List로 대체하자

  - a[2:5]=[]

    ![1561978405473](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561978405473.png)

#### List 함수/메소드

##### list() 

- 인자값으로 주어지는 List, 문자열 등을 List로 변환하는 함수

  ![1561978603865](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561978603865.png)

##### append()

- 맨 마지막 인덱싱 요소에 값을 추가하는 함수 

- 맨 마지막 인덱스에 값을 추가하는 것으로 인덱스가 단 1개만 늘어난다.

- 인자로 값 또는 List를 부여할 수 있다. 

  ![1561978722801](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561978722801.png)

##### extend()

- 맨 마지막 인덱싱 요소에 리스트/문자열을 추가하는 함수 (정수는 대괄호에 싸은 후 삽입)

- append()와는 달리, List를 늘리기 때문에, 인덱스가 삽입하는 List의 크기만큼 늘어난다. 

  ![1561978978274](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561978978274.png)

##### sort()

- 오름차순으로 정렬하는 함수 

  ![1561979184489](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561979184489.png)

- 자기자신(원본)을 정렬하기 때문에 return 되는 값이 없다.

- result = my_list.sort()를 수행하면, result에는 값이 없기 때문에 None이 출력된다. 

  ![1561979233937](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561979233937.png)

##### reverse()

- 현재의 List를 거꾸로 만드는 함수 

- sort() 이후 reversre()를 하면, 내림차순으로 정렬하는 효과를 얻을 수 있다.

  ![1561979400641](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561979400641.png)

##### index()

- 인자로 주어진 값의 인덱스를 리턴하는 함수 

- 해당 List에 값이 없을 때는 오류 메시지가 발생한다.

  ![1561979523466](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561979523466.png)

## Python Sequence Type : Tuple

- 하는 일은 List와 거의 유사하지만, List와 표현 방법이 다르다.
  - Tuple : ( )
  - List : [ ]
- ReadOnly 이고 원본의 수정과 삭제가 불가하다. 

#### Tuple의 생성

- 공백 Tuple 생성

  - a = ()

    ![1561979954224](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561979954224.png)

- Tuple 생성

  - a = (1,2,3)

    ![1561979971080](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561979971080.png)

  - 요소가 1개인 Tuple은 숫자 혹은 문자열로 표현될 수 있기 때문에 Tuple을 표현하기 위해서는 별도의 표현이 필요하다. 

    - **a = (1,)**

      ![1561980089760](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980089760.png)

  - ( ) 자체를 생략할 수 있다. 

    ![1561980144049](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980144049.png)

    

  - Tuple을 통해 각각의 변수에 값을 바인딩 할 수 있다.

    - a = 10
    - b = 20
    - c = 30

    ![1561980205248](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980205248.png)

#### Tuple(원본)의 수정

- 원본이 수정과 삭제가 불가하다.

#### Tuple 인덱싱 (Indexing)

- Tuple의 위치를 지정하여 해당 위치의 Tuple 값을 알아낸다. 

  ![1561980361840](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980361840.png)

#### Tuple 슬라이싱 (Slicing)

- Tuple 슬라이싱의 결과는 Tuple

- 주어진 영역 내의 Tuple 값을 복사한다.

  ![1561980437023](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980437023.png)

#### Tuple의 연산

- 원본에 의한 수정과 삭제는 불가하지만, 새로운 Tuple을 생성하는 +와 *는 연산이 가능하다.

  - +연산은 2개의 Tuple을 합한다. 

  - *연산은 해당 튜플을 곱하는 숫자 만큼 더한다.

    ![1561980632473](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980632473.png)

#### Tuple과 List의 변환

##### tuple() 

- List를 Tuple로 변환한다. 

  ![1561980791809](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980791809.png)

##### list()

- Tuple을 List로 변환한다. 

  ![1561980834489](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561980834489.png)



## Python Sequence Type : Range

- 숫자의 sequence를 가지는 집합으로 주로 for문에서 사용한다. 
- Java의 forEach()문과 유사하다.

#### Range 생성

- range(시작, 끝) 

  - 시작부터 1씩 증감하여 끝 -1 까지의 범위
  - 끝은 Exclusive로 포함되지 않는다.
  - range(10,20) ==> 10~19

- range(시작, 끝, 증감)

  - 시작부터 증감 만큼 증감하여 끝 -1 까지의 범위

  - range(10,20,3) ==> 10,13,16,19

    ![1561982266864](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561982266864.png)

- range(끝)

  - 처음 (0) 부터 1씩 증감하여 끝 -1 까지의 범위
  - range(10) ==> 0~9

#### Range 인덱싱 (Indexing)

- 포함되는 범위의 인덱스의 값을 가져온다.

- my_range(10,20,3)은 10,13,16,19을 가지며, my_range[-1]은 19가 된다.

  ![1561982421449](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561982421449.png)

#### Range 슬라이싱 (Slicing)

- Range 슬라이싱의 결과는 Range

- range(10,20,3)인 my_range[:2]의 값은 10, 13 만 복사되므로, range(10,16,3)이 된다.

  ![1561982762818](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561982762818.png)

#### Range를 이용한 for 문

- Java의 forEach()문과 유사하다.

- Python의 for 문

  1. for 키워드의 끝에는 반드시 콜론(' : ')이 필요하다.
  2. 소/중괄호 등의 별도의 블록 지정을 하지 않고, 콜론(' : ') 뒤에서 엔터를 치고 들여쓰기 (Indentation : space 4번, tab 1번) 를 통해 블록을 지정한다. 
  3.  들여쓰기를 한 후에는 반드시 수행할 함수 혹은 일을 작성해야한다. 만약, 특별히 수행할 일이 없을 경에는 예약어 pass를 작성한다.

  ![1561983152683](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561983152683.png)

## Python Mapping Type : Dict (: Dictionary)

- java의 Map과 같은 기능을 제공하고, Key-Value 쌍으로 존재한다.

- Python의 dict은 JSON 형식으로 표현한다.

  ```python
  {"name" : "홍길똥", "age" : 2}
  ```

- Key값이 중복되는 경우, Syntax Error가 발생하기 때문에 중복되지 않는 Key값을 사용해야 한다.

  ![1561983842594](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561983842594.png)

#### Dict 생성

-  JSON 표현법으로 생성한다.

  ![1561983403753](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561983403753.png)

- type()

  - type 확인하기

  ![1561983448585](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561983448585.png)

#### 새로운 Dict 추가

- Key-Value쌍으로 Dict에 추가한다. 

- my_dict[Key값] = "Value 값"

  ![1561983623130](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561983623130.png)

#### 기본의 Dict 삭제

- Key값으로 특정 Key-Value를 삭제한다.

- del my_dict[Key 값]

  ![1561983692473](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561983692473.png)

#### Dict의 함수

##### keys() 

- Dict의 모든 Key값을 리턴한다. 

- 리턴값은 List처럼 생긴 객체로, 실제 List는 아니므로 List의 함수를 사용할 수 없다.

  ![1561983978865](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561983978865.png)

##### values()

- Dict의 모든 Value값을 리턴한다.
- 

