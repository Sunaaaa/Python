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

## 내장상수 

1. True : 참

2. False : 거짓

3. None : 값이 존재하지 않음을 의미한다.

   ![1561707741813](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561707741813.png)

## 내장형 데이터 타입(Built - in Type)

- 이미 Python에 내장되어 있는 데이터 타입

### 숫자형 (Numeric Type)

- int, double 등의 숫자형 type을 명시했던 Java와 달리, Python에서는 별도의 숫자형 type을 명시하지 않아도 자동으로 해당 타입으로 바인딩되고 인식한다. 

  - a= 123	=> 정수

  - b= 3.1415926535	=> 실수

  - c= 3.14E10	=> 실수 (지수 형태로 표현, c = 3.14* 10의 10승)

    

    ### 연산 

    - div = 3/4	=> 결과값은 실수

      - 정수와 정수 연산의 결과값이 정수인 Java와 달리, Python에서는 연산의 결과값을 실수로 출력한다.

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

  ![1561709903363](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561709903363.png)

#### 문자열 슬라이싱(Slicing)

- 문자열의 원하는 부분만 뽑는다.

- [ : ] : ' : '를 기준으로 왼쪽은 inclusive(포함)이고, 오른쪽은 exclusive(불포함)이다. 

  - text[1:3] : text의 1,2번 인덱스만 뽑는다.

  - text[:3] : text의 처음부터 3번 인덱스 전까지만 뽑는다. (1,2번 인덱스만 뽑는다.)

  - text[3:] : text의 3번 인덱스부터 끝까지 뽑는다. 

  - text[:] : text의 처음부터 끝까지, 문자열 전체를 뽑는다.

    ![1561710273933](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561710273933.png)

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

- text = 숫자와 숫자로 바인딩된 변수를 동시에 사용하여 값을 표현한다.

  ![1561710963774](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561710963774.png)

#### 문자열 내장 함수

##### len() 

- 문자열의 길이를 구하는 함수 

- 내장함수 이므로 인자값으로 문자열을 받는다.

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





- 코드가 몇번째 실행되었는지 알 수 있음

![1561700396474](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561700396474.png)

-  셀 =  edit mode

- ![1561701871662](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561701871662.png)

- 셀 밖을 누르고 b를 하면 아래에 새로운 셀이 생김
- ![1561701906549](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561701906549.png)

- dd를 누르면 해당 셀을 지울 수 있음
- z 키로 undo를 수행한다.
- Ctrl + /  : 잡은 영역만큼 한번에 주석











- 타입이 다른 경우, 연산 시

  ![1561702540616](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561702540616.png)

- 타입 변환을 직접 명시하여 처리해야함

  ![1561702668773](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561702668773.png)

- 문자열 3번 연속으로 concat

  ![1561702761676](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561702761676.png)

- 배열처럼

  ![1561703062061](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561703062061.png)

- 앞에서 부터 인덱싱 : 0,1,2,3,4....

- 뒤에서 부터 인덱싱 : -1, -2, -3 ...

  ![1561703145509](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561703145509.png)

- slicing

  ![1561703248195](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561703248195.png)

  ![1561703433614](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561703433614.png)

- 문자열 Formatting

  ![1561703916884](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561703916884.png)

  ![1561703983300](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561703983300.png)

  - 복수개 

    ![1561704178493](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1561704178493.png)
