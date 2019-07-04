# Pandas

- Python의 데이터 분석의 핵심 Module( package )

- 데이터 분석 방법 

  1. EDA( 탐색적 데이터 분석 )
     - 엑셀을 이용하여 데이터를 분석한다.
     - Python으로 Pandas를 이용해서 EDA 수행
  2. 통계적 데이터 분석
     - 통계적 이론을 이용하여 데이터를 분석한다.
  3. Machine Learning 
     - 기존의 데이터를 이용하여 프로그램을 학습시킨다. 학습된 결과를 이용해 예측한다.

- Numpy를 사용하기 위해 numpy module을 시스템에 설치 

  - conda install numpy

    ```python
    import pandas as pd
    ```

    

- Pandas의 자료구조 

  - Series 
  - DataFrame

- display()

  - Series와 DataFrame의 전체 구조를 출력할 때 사용한다.
  - 구조가 아닌 특정 값을 출력할 때는 print()를 사용한다.



## Series 

- Numpy Array와 상당히 유사하다.
- 동일한 데이터 타입으로 복수개의 요소로 구성된다.

### pd.Series( )

- Series를 생성하는 함수

  - List를 이용하여 Series 생성

    - 첫번 째 인자로 Series로 생성할  List를 제공한다.

    - 두번 째 인자로 Series의 데이터 타입을 제공한다.

    - Python의 List와는 다르게, Series는 인덱스와 데이터 값을 함께 출력한다.

      ![1562227066726](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562227066726.png)

      

    - 별도의 인덱스 지정하여 Series 생성

      - 문자, 날짜, 성별 등 다양한 속성을 이용하여 사용자가 원하는 인덱스로 Series를 생성할 수 있다.
      - 기존의 순번 인덱스 ( 1,2,3,... )로도 접근이 가능하다.
      - Series 생성
        - s = pd.Series( [ List ], index=[ List ] )
        - Series를 생성할 List와 동일한 크기의 List를 이용하여 Index를 설정한다.

    - Series의 인덱스 접근 

      - s[1] : 1번 인덱스의 데이터

      - s['a'] : 인덱스가 'a'인 곳의 데이터

      - s[1:2] : 1번 인덱스의 데이터

      - s['c':'k'] : 인덱스가 'c'인 곳부터 'k'인 곳까지의 데이터 ( 사용자 지정 인덱스는 슬라이싱 시, 양쪽 모두 포함으로 슬라이싱을 수행한다. )

        ![1562228146254](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562228146254.png)

    

    

    - #### [ Series ].values

      - 해당 Series 안의 데이터/Value 만 1차원의 Numpy Array로 리턴한다.

        ![1562227466254](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562227466254.png)

    - #### [ Series ].index

      - 해당 Series 의 인덱스의 range가 리턴된다.

        ![1562227484836](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562227484836.png)

    - #### [ Series ].dtype

      - 해당 Series 의 데이터 타입이 리턴된다.

        ![1562227506804](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562227506804.png)

    - #### [ Series ].sum( )

      - 해당 Series 내의 모든 데이터 값의 총합.

        ![1562228189572](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562228189572.png)

        

  - Dict을 이용하여 Series 생성

    - Python의 Dict을 이용해 Series를 생성할 수 있다.

    - Dict의 Key-Value가 Series의 Index, Data로 Mapping  되기 때문에 별도의 Key값을 설정할 필요가 없다.

    - 인자로 Dict를 제공하기만 하면 Series 가 생성된다.

      ![1562228363221](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562228363221.png)

    - #### [ Series ].name

      - 해당 Series 의 이름을 설정한다.

        ![1562228522366](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562228522366.png)

      

    - #### [ Series ].index.name

      - 해당 Series 의 인덱스의 이름을 설정한다.

        ![1562228542599](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562228542599.png)





## DataFrame

- Table 형식으로 구성된 자료구조

- 2차원 배열, 데이터 베이스의 테이블과 상당히 유사하다.

  ( 테이블의 데이터  타입은 다양할 수 있지만, 특정 컬럼 내의 데이터 타입은 반드시 동일해야 한다.)

- 대부분의 경우에 DataFrame을 이용해 데이터 분석을 수행한다.

  

  ### pd.DataFrame( )

  - Dict를 이용해서 DataFrame 생성

    - Python의 Dict을 이용해서 Data Frame/ 테이블을 생성할 수 있다.

    - 인자로 Dict를 제공한다.

    - Key값에 단 하나의 Value값만 존재하는 Python의 Dict과는 달리, DataFrame은 하나의 Key값에 여러개의 Value값이 존재한다. ( Value 값은 List, 배열 등의 형태이다. )

      ![1562228919847](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562228919847.png)

    - #### [ DataFrame ].shape

      - 해당 DataFrame 의 형태를 출력한다.

        

    - #### [ DataFrame ].size

      - 해당 DataFrame 의 요소 개수를 출력한다.

      - 인덱스와 컬럼은 포함되지 않고, 실제 데이터들만 포함하여 계산한다.

        

    - #### [ DataFrame ].ndim

      - 해당 DataFrame 의 차원을 출력한다.

        

    - #### [ DataFrame ].index

      - 해당 DataFrame 의 인덱스를 range의 형태로 출력한다.

        

    - #### [ DataFrame ].columns

      - 해당 DataFrame 의 컬럼에 대한 정보를 출력한다.

        

    - #### [ DataFrame ].values

      - 해당 DataFrame 의 값들을 Numpy Array의 형태로 출력한다.

    

    

    - DataFrame의 정보 출력

    ![1562229388307](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562229388307.png)

### pd.read_csv( )

- CSV 파일을 이용해 DataFrame을 생성할 수 있다.

- CSV 파일의 첫번 째 행은 컬럼을 명시하므로, 첫줄은 '#'을 붙여 주석 처리한다.

- 인자로 CSV 파일의 위치를 제공한다.

  ![1562229682140](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562229682140.png)

  - #### [ DataFrame ].head( )

    - 테이블의 처음부터 인자로 주어지는 정수만큼의 개수만 출력한다.

      ![1562229762310](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562229762310.png)

  - #### [ DataFrame ].tail( )



# 데이터 전달 포맷

## 1. CSV 

- Comma Separated Value 
- ' , '를 기준으로 데이터들이 분리되어있다.
- 부가적인 데이터가 많지 않아서 대용량의 데이터를 표현할 때 적합