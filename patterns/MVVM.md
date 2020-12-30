PATTERN MVVM
===========
![MVVM pattern](/image/MVVM.png)

## 모델-뷰-뷰모델

#### 1. 구조
- Model: 앱에서 사용되는 데이터와 그 데이터를 처리
- View: 사용자에게 보여지는 UI
- View Model: View를 표현하기 위해 만든 View를 위한 Model. View를 나타내기 위한 Model이자 View를 나타내기 위한 데이터를 처리

#### 2. 동작
1) 사용자의 action이 view를 통해 들어옴
2) view에 action이 들어오면 command 패턴으로 view model에 action 전달
3) view model은 model에게 데이터 요청
4) model은 view model에게 요청받은 데이터 응답
5) view model은 응답받은 데이터를 가공하여 저장
6) view는 view model과 data binding하여 화면 표시

#### 3. 특징
- MVVM 패턴은 Command 패턴과 Data Binding 패턴 두 가지를 사용하여 구현됨
- command 패턴과 data binding을 이용해 view와 view model 사이의 의존성을 없앰
- view model과 view는 1:n 관계

#### 4. 장단점
- 장점: MVVM 패턴은 View와 Model 사이의 의존성이 없음   
        [Command 패턴](https://ko.wikipedia.org/wiki/%EC%BB%A4%EB%A7%A8%EB%93%9C_%ED%8C%A8%ED%84%B4)과 [Data Binding 패턴](https://en.wikipedia.org/wiki/Data_binding)을 사용하여 View와 View Model 사이의 의존성 또한 없앰   
        각각 독립적이기 때문에 모듈화 하여 개발 가능
- 단점: view model의 설계가 쉽지 않음 

&reference    
[site](https://beomy.tistory.com/43)
