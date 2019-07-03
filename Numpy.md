# Numpy 

1. Numpy를 사용하기 위해 numpy module을 시스템에 설치 
   - conda install numpy
   - pip install numpy (파이썬 install manager을 사용해서 numpy 설치)
   - numpy라는 모듈을 repository에서 찾아서 설치하게 됨

```
import numpy as np
```

- Vector와 Matrix 연산에 상당한 편의성을 제공한다.
- 그 자체로 의미가 있다기 보다는 다른 모듈에 대한 기본 자료구조로 많이 사용된다. 
  - Numpy의 Array가 많이 사용된다.
  - Pandas와 Matlotlib (그래프 그리기) 의 기본 자료구조로 이용된다.
- Aliasing 은 np로 통일

- 자주 사용되는 자료구조 
  - 다차원 배열 (n-dimensional Array) = numpy array
    - Python의 List (서로 다른 타입의 데이터가 들어갈 수 있다.) 와 유사함
    - 그러나, numpy array는 같은 타입의 데이터를 사용해야한다. 다른 타입의 데이터를 문자열로 변환시켜 저장한다.
    - Python의 List 보다 메모리 사요이나 속도 면에서 상당히 효율적이고 빠르다.

## Numpy Array 생성

### List 와 Numpy Array의 데이터 타입

- Python의 List와 Numpy Array의 데이터 타입은 다르다.

-  Python의 List 

  - list 라는 클래스의 인스턴스를 생성하는 것

  - List 생성과 타입

    ![1562135795556](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562135795556.png)

  - List 요소 데이터와 타입

    ![1562135841755](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562135841755.png)

- Numpy Array

  - 생성과 타입

    ![1562136128891](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562136128891.png)

  - Numpy Array 요소 데이터와 타입

    ![1562136175963](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562136175963.png)

    

###  1. np.array()

- 기존의 List, Tuple등을 이용해서 인자로 이용해 Numpy Array로 변환하는 함수

- Numpy Array 내의 데이터 타입은 동일해야 한다.

- 1차원 Numpy Array

  - Vector 이므로 1차원 배열의 형태로, ' , ' 가 없다. 

  - 1차원 배열 생성

    ![1562136316035](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562136316035.png)

  - 1차원 배열 요소 접근

    - [ 인덱스 ] 의 표현식으로 1차원 배열에 접근한다.

      ![1562138329987](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562138329987.png)

  - 실수형 1차원 배열 생성

    - array()의 두번째 인자로 배열 요소의 데이터 타입을 지정할 수 있다. ( 예 . dtype=np.float64)

      ![1562138542163](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562138542163.png)

    

- 2차원 Numpy Array

  - List의 List를 이용하여 n행 n열의 배열을 생성한다.

  - 2차원 배열 생성

    ![1562138002860](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562138002860.png)

  - 2차원 배열의 요소 접근

    - [ 행,열 ] 의 표현식으로 2차원 배열에 접근한다.

    ![1562138137011](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562138137011.png)

  - 실수형 2차원 배열 생성

    - array()의 두번째 인자로 배열 요소의 데이터 타입을 지정할 수 있다. ( 예 . dtype=np.float64)

      ![1562138491796](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562138491796.png)

- 만약, 데이터 타입이 서로 다른 경우에는 모든 요소의 데이터 타입을 문자열로 변환해서 Numpy Array를 생성한다.

  ![1562136497723](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562136497723.png)

### 2. np.zeros( )

- 주어진 행과 열의 크기만큼  숫자 0으로 채워진 배열을 생성하는 함수 

- 인자로 행과 열의 크기를 Tuple로 전달한다.

  ![1562141604315](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562141604315.png)

### 3. np.ones( )

- 주어진 행과 열의 크기만큼  숫자 1로 채워진 배열을 생성하는 함수 

- 인자로 행과 열의 크기를 Tuple로 전달한다.

  ![1562141660139](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562141660139.png)

### 4. np.empty( )

- 주어진 행과 열의 크기만큼  배열을 생성하는 함수 

- 이때, 초기값을 지정하지 않았기 때문에 초기값이 랜덤으로 들어간다.

- 인자로 행과 열의 크기를 Tuple로 전달한다.

  ![1562141813295](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562141813295.png)



### 5. np.full( )

- 주어진 행과 열의 크기만큼, 주어진  초기값과 초기값의 타입으로 배열을 생성하는 함수 

- 첫번째 인자로 행과 열의 크기를 Tuple로 전달한다.

- 두번째 인자로 초기값을 전달한다.

- 세 번째 인자로 초기값의 타입을 전달한다.

  ![1562141999227](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562141999227.png)

  ![1562142022740](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562142022740.png)



### 5. np.arange( )

- 시작은 포함, 끝은 불포함, 주어진 간격 만큼의 배열을 생성하는 함수 

- 내가 정한 영역 안에서 내가 원하는 간격으로 배열을 만들 수 있다.

- 인자는 ( 시작, 끝, 간격 )의 형태로 전달된다. ( range와 유사한 매커니즘 )

  ![1562142189709](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562142189709.png)

## Numpy Array 함수 

### 1. [Numpy Array].ndim()

- 해당 Numpy Array가 몇 차원의 배열인지를 출력하는 함수

  ![1562139189186](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562139189186.png)

### 2. [Numpy Array].shape()

- 해당 Numpy Array의 형태를 Tuple로 표현하여 출력하는 함수 

- (4, ) : 1차원 배열이고, 데이터가 4개가 존재한다.

- (4, 4) : 2차원 배열이고, 4개의 행, 4개의 열 

  ![1562139210764](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562139210764.png)



### 3.[Numpy Array].size()

- 행과 열에 관계없이, 해당 Numpy Array안 데이터의 총 개수를 출력하는 함수

  ![1562139234155](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562139234155.png)



### 4. len ( [Numpy Array] )

- 행의 길이를 출력하는 함수.

- 2차원 배열의 경우, len(arr[0]) 을 이용하여 행의 길이를 알 수 있다.

  ![1562139327636](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562139327636.png)

### 5. [Numpy Array].dtype()

- Numpy Array 내의 데이터 타입을 확인하는 함수

  ![1562136393219](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562136393219.png)



### 6. [Numpy Array].astype( )

- 배열을 다른 데이터 타입의 배열로 변환하는 함수

- 변환하고자 하는 데이터 타입을 인자로 받는다. 

- 실수 배열 ( float64 ) -> 정수 배열 ( int32 )( 소수점은 버림 연산 )

  ![1562141237172](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562141237172.png)

- 정수 배열 ( int32 ) -> 실수 배열 ( float64 )

  ![1562141289131](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562141289131.png)



### 배열 구조 파악 함수 총 정리

![1562139725071](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562139725071.png)

예 )  [ ] 와 ' , '를 제외하고 배열을 출력하기

```python
import numpy as np

my_list = [[1,2,3],[4,5,6],[7,8,9],[10,11,12]]
arr = np.array(my_list)
print(arr)

# for 문을 적절히 이용해서 numpy array안의 데이터를 행렬형태로 출력하세요
'''
1  2  3
4  5  6
7  8  9
10 11 12
'''
# for val in range(len(arr)):
#     for val2 in range(0,len(arr[val])):
#         print(arr[val,val2], end=" ")
#     print("")

for i in range(arr.shape[0]):
    print()
    for j in range(arr.shape[1]):
        print(arr[i,j], end=" ")

```



## 배열의 구조 변경

- 데이터의 크기가 변경 전과 후와 같아야 한다.
- don't care 키워드 **<u>' -1 '</u>** 을 사용하여 다른 설정을 우선 순위로 수행한뒤, 자동으로 값이 설정된다. 

### 1. [ Numpy Array ].shape 

- 1차원 : ( 데이터의 총 개수 ,)

- 2차원 : ( 행, 열)

- 3차원 : ( 깊이, 행, 열)

  ![1562140684677](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562140684677.png)

- shape()은 해당 배열의 원본 자체의 구조를 변경하기 때문에, 사용되는 경우가 드물다.

### 2. [ NumpyArray ].reshape( )

- 새로운 Numpy Array View가 생성된다. 

  - 매번 배열이 복사되는 경우에는 메모리 낭비가 심하기 때문에 메모리의 효율성을 위해 View를 만든다. 

  - View 

    - 형태만 다를 뿐, 원본 데이터를 공유한다. 
    - 원본이 변경 되면, View도 함께 변경된다.

    ![1562142860406](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562142860406.png)

    - reshape( 행,열 ).copy() 

      - 새로운 Numpy Array View의 복사본으로 원본이 변경되어도 변경되지 않는다.

        ![1562143024998](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562143024998.png)



### 3. [ Numpy Array ]. reval( )

- 다차원 배열을 1차원으로 변환하는 함수

- 원본과 데이터를 공유하고 형태만 1차원인 새로운 Numpy Array View가 생성된다. 

  ![1562143242717](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562143242717.png)

### 4. [ Numpy Array ]. resize( )

- 주어진 배열을 View가 아닌 완전한 복사본을 생성한다. 

- ( 바꿀 배열, 바꿀 형태 )의 형태로 인자를 전달한다.

- 완전한 복사본이기 때문에 원본의 변경이 적용되지 않는다.

  ![1562143429838](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1562143429838.png)

# Matplot

