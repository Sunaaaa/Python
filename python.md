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

  