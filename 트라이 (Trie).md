# 트라이 (Trie)

- digital-tree, prefix-tree
- 트리 구조의 알고리즘
- 검색이 빠르다.
- 노드가 키를 갖지 않는 대신, 해당 위치가 키의 역할을 한다.
- 한 노드와 연관된 문자열은 해당 노드의 공통 접두어이다.



### 트라이 구조

- 문자열 집합 my_list의 트라이 구성

  ```python
  my_list = {'BE','BEE','BUS','TEA','TEN'}
  ```

  - root node는 빈 node
  - 부모 node에 접미 문자를 하나씩 붙여 자식 노드를 만든다.
  - edge는 접미 문자가 붙는 것을 나타낸다.
  - 문자열이 끝나는 곳은 Terminal node
  - root에서 terminal node 까지의 문자를 모으면 검색어 발견!



### Python Module : Collections

- Tuple  : index를 기준으로 접근

  - 메소드

    ```python
    t = 1,2,3,4
    t.count(3) # tuple 내의 특정 원소의 개수
    t.index(2) # tuple 내의 특정 원소의 위치
    ```

- NamedTuple : 키를 가지고 접근

  - tuple을 보다 명시적으로 사용하기 위해 name으로 접근
  - tuple의 sub Class를 만드는 factory 기능을 처리