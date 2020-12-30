PATTERN MVP
===========
![MVP pattern](/image/Model_View_Presenter_GUI_Design_Pattern.png)

## 모델-뷰-프리젠터
- MVC(Model-View-Controller) 아키텍처 패턴의 파생 패턴(Controller 대신 Presenter가 존재)
- 사용자 인터페이스를 개발하기 위해 대부분 사용됨
- 프리젠터는 "middle-man"을 담당
- 모든 프레젠테이션 로직은 프리젠터로 넘어감

#### 1. 구조
- Model: 앱에서 사용되는 데이터와 그 데이터를 처리
- View: 사용자에게 보여지는 UI
- Presenter: View에서 요청한 정보로 Model을 가공해 View에게 전달, View와 Model의 이음새 역할

#### 2. 동작
1) 사용자의 action이 view를 통해 들어옴
2) view는 데이터를 presenter에게 요청
3) presenter는 model에게 데이터 요청
4) model은 presenter에게 요청받은 데이터 응답
5) presenter는 view에게 데이터를 응답
6) view는 presenter가 응답한 데이터를 이용하여 화면 표시

#### 3. 특징
- presenter는 view와 model의 인스턴스를 가지고 있어 둘을 연결하는 이음새 역할
- presenter와 view는 1:1 관계

#### 4. 장단점
- 장점: presenter를 통해서만 데이터를 전달받기 때문에 view와 model의 의존성이 없음
- 단점: 앱이 복잡해질수록 view와 presenter 사이의 의존성이 높아짐

&reference   
[todoMVP - google architecture sample](https://github.com/android/architecture-samples/tree/todo-mvp)   
[site](https://beomy.tistory.com/43)
