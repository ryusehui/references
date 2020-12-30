css units
=========

### [요약]
### 1. em
  - 현재의 폰트 사이즈 지정
  - font-family에 의존
  - 부모 element의 폰트 사이즈 x 지정 em
  - body 태그에 em 값으로 폰트 사이즈를 지정하면 모든 자식 요소들은 영향을 받음

### 2. rem: root em
  - font-family에 의존
  - 최상위 요소의 폰트, 너비, 높이 등의 사이즈를 기준으로 함
  - 그리드 시스템에서도 유용하게 사용 가능
  
### 3. vh: vertical height & vw: vertical weight
  - 뷰포트의 너비와 높이 값에 맞게 사용 가능
  - 각 요소는 값의 1/100 단위
  - 가로 세로 중에서 작은 값에 따라 vmin이 정해지고, 큰 값에 따라 vmax가 정해짐
  - 폰트 사이즈 등에 사용 가능

### 4. vmin & vmax
  - 너비, 높이 값의 최대/최소 값 지정
  - 각 요소는 값의 1/100 단위
  
### 5. ex & ch
  - em, rem과 비슷
  - 폰트의 특정 수치에 기반
  - ch: 0의 너비 값의 "고급 척도"로 정의됨
    - width: 40ch;는 40개의 문자열을 포함한다는 의미
  - ex: 현재 폰트의 x-높이(소문자 x의 높이) 값 또는 em의 절반 값
    - 폰트의 중간 지점을 알아내기 위해 자주 사용
    - 브라우저는 위첨자와 아래첨자를 vercial-align으로 정의하고 있지만   
    보다 정교하게 정렬하기 위해 위첨자는 bottom: 1ex;로 아래첨자는 bottom: -1ex;로 지정
---
&reference
- [units reference](https://webclub.tistory.com/356)
