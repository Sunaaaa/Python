- 가 ~ 핳

  ```python
  for i in range(11172):
      print(chr(44032 + i) , end='')
  ```

- Enumerate

  ```python 
  names = ['가', '나', '다', '라', '마']
  
  for i in range(len(names)):
  	print('{} 번 {}'.format(i+1,name))
  
  ```



모듈 : 미리 만들어진 코드를 가져와 쓰는 방법

- import <모듈 이름>

- math 모듈

  ```python
  import  math
  
  r = 10
  print(2 * math.pi * r)
  
  math.ceil(2.5) # 3
  math.floor(2.5) #2
  ```

  

- random 모듈

  ```python
  import random
  candidate = ['가위','바위','보']
  selected = random.choice(candidate) # 후보로 받은 list중 하나를 무작위로 
  
  '''
  print('가위? >> ', selected == '가위' )
  
  '''
  
  ```

  

- urllib.request 모듈

  ```python
  del get_web():
      import urllib.request
  
      # 받은 url을 연다
      response = urllib.request.urlopen(url)
  
      # 데이터를 읽는다.
      data = response.read()
  
      # 사람이 읽을 수 있도록 디코딩
      decoded = data.decode()
  
      return decoded
  
  url = input('웹페이지 주소')
  
  content = get_web(url)
  print(content)
  
  
  ```

  

- random.choice(Non-Emptyseq list)

  : 비어있지 않은 list 중 임의의 0Element 하나를 반환  

  ```python
  import random
  list = ["빨","주","노","초","파","남","보"]
  random_element = 
  random.choice(list)
  
  print(random_element)
  ```

  

- random.randint(a,b) 

  : a <= N <= b 사이의 난수 생성

  ```python
  import random
  
  random_number = random.randint(2,5)
  ```

  

- random.shuffle(list)

  : list내의 element들을 섞는다.

  : 인자로 전달된 배열 자체를 shuffle한다. 

  ```python
  import random
  list = ["빨","주","노","초","파","남","보"]
  
  random.shuffle(list)
  print(list)
  ```

  

- 가위 바위 보 

  ```python
  wintable ={
      '가위' : '보',
      '바위' : '가위',
      '보' : '바위'
  }
  
  def rsp (mine, yours):
      if mine==yours:
          return "draw"
      elif wintable[mine] == yours:
          return "win"
      else:
          return "lose"
      
  result = rsp('가위','바위')
  print(result)
      
  messages = {
      'win' : '이겼다!',
      'lose' : '졌다..',
      'draw' : '비겼다!'
  }
  
  print(messages[result])
  ```

  

- 딕셔너리 수정하기 

  - 딕셔너리 추가

    : 해당 딕셔너리에 새로운 Key값- Value값을  넣어준다.

    ```python 
    dict = {
        'one' : 1,
        'two' : 2,
    }
    dict['three'] = 3
    ```

  - 딕셔너리 수정

    : 해당 딕셔너리의 값을 수정한다. 

    ```python 
    dict['one'] = 11
    
    days_in_month = {"1월":31, "2월":28, "3월":31}
    days_in_month['2월'] = 29
    
    
    print(days_in_month)
    ```

  - 딕셔너리 삭제

    : 주어진 Key값으로 해당 딕셔너리의 특정 값을 삭제한다. 

    ```python
    del(dict['one'])
    dict.pop('two')
    ```

  - 딕셔너리 반복문

    - key 값 

      ```python
      for key in ages.keys():
          print(key)
      ```

    - value 값

      ```python
      for value in ages.values()
      	print(value)
      ```

    - key값과 value 값

      ```python
      for key, value in ages.items():
          print('{}의 나이는 {} 입니다.'.format(key, value))
      ```

  - List와 비교 

    - 공통점

    |           |      List      |        Dictionary         |
    | :-------: | :------------: | :-----------------------: |
    |   생성    | list = [1,2,3] | dict = {'one':1, 'two':2} |
    |   호출    |    list[0]     |        dict['one']        |
    |   삭제    |  del(list[0])  |     del(dict['one'])      |
    | 개수 확인 |   len(list)    |         len(dict)         |
    |  값 확인  |   2 in list    |   'two' in dict.keys()    |
    | 전부 삭제 |  list.clear()  |       dict.clear()        |

    - 차이점

    |      |                           List                           |                          Dictionary                          |
    | :--: | :------------------------------------------------------: | :----------------------------------------------------------: |
    | 순서 | 삭제 시, 순서가 바뀌기 때문에 인덱스에 대한 값이 바뀐다. |       key로 값을 가져오기 때문에 삭제 여부와 상관없다.       |
    | 결합 |                      list1 + list2                       | dict1.update(dict2) ( : 딕셔너리에서 새로운 딕셔너리를 합치기 ) |

  - 실습 1

    ```python
    # 만약 box에 불량품이라는 이름표가 있으면 box 전체를 빈 딕셔너리로 만들어 버리고, 불량품이 없으면 box를 그대로 두는 함수
    def check_and_clear(box):
        if '불량품' in box.keys():
            box.clear()
        else:
            pass
            
    box1 = {"불량품" : 10}
    check_and_clear(box1)
    # {}가 출력되어야합니다.
    print(box1)
    
    box2 = {"정상품": 10}
    check_and_clear(box2)
    # {"정상품": 10}가 출력되어야합니다.
    print(box2)
    ```

  - 실습 1

    ```python
    # products는 문방구에 진열되어 있는 상품과 가격 정보를 담고 있는 딕셔너리입니다. catalog에는 이번에 새로 입고되는 상품과 가격이 적혀있고 또 기존 제품의 가격이 변경된 경우 그 가격정보를 담고 있습니다. products가 catalog의 정보를 반영하여, 앞으로 문방구에서 판매할 상품 정보를 갖는 딕셔너리가 되도록 
    '''
    dict1 = {1 : 100, 2 : 200}
    dict2 = {1 : 1000, 3 : 300}
    dict1.update(dict2)        #{1 : 1000, 2 : 200 : 3 : 300}
    '''
    
    products = {"풀":800, "딱풀":1200, "색종이":1000,"색연필":5000,"스케치북":3500}
    
    catalog = {"겨울용 실내화":12000, "잠자리채":8000, "딱풀":1400}
    
    // 
    print(products.update(catalog))
    ```



- 튜플 

  - 한번 정해진 순서를 바꿀 수 없다. 

  - 튜플은 값의 변경과 삭제가 불가능

  - 튜플 선언 

    ```python
    tuple1 = (1, 2, 3, 4)
    
    tuple2 = 1, 2, 3, 4
    
    mylist = [1,2,3,4]
    tuple3 = tuple(mylist)
    
    tuple1 = (11, 22, 33)
    for i in range( len( tuple1) ):
        print( tuple1[i] )
    ```

  - packing 

    : 하나의 변수에 여러개의 값을 넣는 것

  - unpacking

    : 패킹된 변수에서 여러개의 값을 꺼내오는 것

    ```python 
    c = (3,4)
    
    # c의 값을 언패킹하여 d,e에 값을 넣었다.
    d ,e = c
    
    # 변수 d와 e를 f에 패킹
    f = d,e
    
    
    
    x = 5
    y = 1
    temp = x
    x = y
    y = temp
    # x = 1, y = 5
    
    x,y = y,x 
    # x = 5, y = 1
    ```

  - 튜플 리스트 활용 

    ```python
    list = [1,2,3,4,5]
    for k,v in enumerate(list):
    	print('{}번째 값 : {}'.format(k,v))    
        
    for a in enumerate(list):
    	print('{}번째 값 : {}'.format(a[0],a[1]))    
        
    for a in enumerate(list):
    	print('{}번째 값 : {}'.format(*a))      
    ```

  - 튜플 딕셔너리 활용

    ```python
    ages = {'T' : 35, 'J' : 23, 'F' : 68}
    
    for k,v in ages.items():
    	print('{}의 나이는 : {}'.format(k,v))    
        
    for a in ages.items():
    	print('{}의 나이는 : {}'.format(a[0],a[1]))    
        
    for a in ages.items():
    	print('{}의 나이는 : {}'.format(*a))      
    ```

- list 의 다양한 기능

  - list.index (value)

    : value를 이용하여 위치를 찾는 기능

    

  - list.extend ([value1, value2])

    : 리스트 뒤에 값을 추가

    ![1564660418219](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1564660418219.png)

  - list.insert (index,value)

    : 원하는 위치에 값을 추가

  - list.sort ()

    : 값을 순서대로 정렬

  - list.reverse()

    : 값을 역순으로 정렬

    

  - List와 문자열

    - List -> 문자열

      ```python
      t_list = ['10','35','27']
      ":".join(t_list)
      # '10:35:27'
      
      w_list = ['Hello','World','는','안녕','세상']
      " ".join(w_list)
      # w = "Hello World 는 안녕 세상"
      
      ```

      

    - 문자열 -> List 

      ```python
      c = list('abcd')
      # ['a','b','c','d']
      
      w = "Hello World 는 안녕 세상"
      w_list = w.split()
      # ['Hello','World','는','안녕','세상']
      
      t = '10:35:27'
      t_list = t.split(":")
      # ['10','35','27']
      ```

  - Slicing

    - ```python 
      list = [1,2,3,4,5,6,7,8,9,10]
      list[1:3:1]
      # [2,3]
      
      list[::-1]
      # [10,9,8,7,6,5,4,3,2,1]
      
      list[::2]
      # [1,3,5,7,9]
      
      list[10:5:-1]
      # [10,9,8,7,4]
      
      del list[:5]
      # 처음부터 5번째까지 삭제
      
      list[1:3] = [77,88]
      list[1:3] = [77,88,99] # 더 많은 개수로 변환
      list[1:4] = [8] # 더 적은 개수로 변환
      ```

    

- while 문 

  ```python
  selected = None
  while selected not in ['가위', '바위', '보']:
      selected = input('가위, 바위, 보 중에 선택하세요>')
      
  print('선택된 값은 : ', selected)
  ```

  ```python
  patterns = ['가위', '바위','보']
  for 
  ```



-  예외처리 

  - Exception

    ```python
    try : # 에러가 발생할 가능성이 있는 코드
    except Exception : # 에러 종류 
        # 에러가 발생했을 경우 처리할 코드
    
    text = '100%'
    try : number = int(text)
    except ValueError:
        print('{}는 숫자가 아니에요.'.format(text))
    ```

    ```python
    def safe_pop_print(list, index):
        try:
            print(list.pop(index))
        except IndexError:
            print('{} index의 값을 가져올 수 없습니다.'.format(index))
            
    safe_pop_print([1,2,3],4)
    
    def safe_pop_print(list, index):
        if index < len(list):
            print(list.pop(index))
        else:
            print('{} index의 값을 가져올 수 없습니다.'.format(index))
            
    safe_pop_print([1,2,3],4)
    ```

    ```python
    try:
        import my_module
    except ImportError:
        print('모듈이 없습니다.')
    ```

  - 에러의 이름을 모를 경우, 발생한 에러의 이름을 받아온다.

    ```python 
    try:
        # 에러가 발생할 가능성이 있는 코드
    except Exception as ex: # 에러 종류
        print('에러가 발생 했습니다', ex) # ex는 발생한 에러의 이름을 받아오는 변수
    ```

    ```python 
    try:
        text = 'abc'
        number = int(text)
    except Exception as ex: 
        print('에러가 발생 했습니다', ex) 
    ```

  - 사용자가 직접 에러를 발생시키는 기능 

    ```python 
    def rsp(mine, yours):
        allowed = ['가위','바위','보']
        if mine not in allowed:
            raise ValueError
        if yours not in allowed:
            raise ValueError
            
    try :
        rsp('가위','바')
    except ValueError:
        print('잘못된 값을 넣었습니다. ')
    ```

    ```python 
    school = {'1반' : [172,185,198,177,165,199],
             '2반' : [165,177,167,180,191]}
    
    for class_number , students in school.items():
        for s in students:
            if s > 190:
                print(class_number, '반에 190을 넘는 학생이 있습니다. ')
                raise StopIteration
                
                
                
    try : 
        for class_number , students in school.items():
            for s in students:
                if s > 190:
                    print(class_number, '반에 190을 넘는 학생이 있습니다. ')
                    raise StopIteration       
                    
    except StopIteration    :
        print('정상종료')
    ```

    

- 단락 평가 

  - 논리연산에서 코드의 앞만 보고 값을 정할 수 있는 경우 뒤는 보지 않고 값을 결정
  - 복잡한 코드를 단순하게 하는 방식

  - And 연산에서 첫 값이 False이면 모두 False

  - Or 연산에서 첫 값이 True이면 모두 True

  - Boolean

    ```python 
    value = input('입력해 주세요') or '아무것도 못 받았어요'
    print('입력받은 값 > ', value)
    ```

    |  구분  |      False       |                True                |
    | :----: | :--------------: | :--------------------------------: |
    |  숫자  |      숫자 0      |      숫자 0을 제외한 모든 수       |
    | 문자열 |  빈 문자열 ("")  |   빈 문자열을 제외한 모든 문자열   |
    |  List  |  빈 리스트 ([])  |   빈 리스트를 제외한 모든 리스트   |
    |  Dict  | 빈 딕셔너리 ({}) | 빈 딕셔너리를 제외한 모든 딕셔너리 |
    |  기타  |  None 오브젝트   |                                    |

- isinstance (값, 자료형) : 자료형 검사 - True, False

  ```python
  isinstance(42, int)
  # True
  
  isinstance(42.0, int)
  # False
  ```



- 인스턴스의 이해 

  ```python 
  list1 = [1, 2, 3]
  list2 = [1, 2, 3]
  
  if list1 is list1:
      print("당연히 list1과 list1은 같은 인스턴스입니다.")
  
  if list1 == list2:
      print("list1과 list2의 값은 같습니다.")
      if list1 is list2:
          print("그리고 list1과 list2는 같은 인스턴스입니다.")
      else:
          print("하지만 list1과 list2는 다른 인스턴스입니다.")
          
          
  # 당연히 list1과 list1은 같은 인스턴스입니다.
  # list1과 list2의 값은 같습니다.
  # 하지만 list1과 list2는 다른 인스턴스입니다.
  ```

  
