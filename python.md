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

  
