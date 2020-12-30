PATTERN MVP
===========
![MVP pattern](/image/Model_View_Presenter_GUI_Design_Pattern.png)
![MVP pattern](/image/MVP.png)

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

> 간단한 동작 예시

> 사용자 입장
> 1) 버튼을 누름
> 2) 버튼 밑에 현재 시간이 뜸

> 앱 입장
> 1) M, V, P 초기화: 앱 생성 시 M, V, P 생성 및 등록
> 2) P -> V: P가 V에게 버튼을 그리라고 시킴
> 3) V: 버튼 그리고 대기
> 4) 사용자가 버튼을 누름
> 5) V -> P: V가 P한테 버튼이 눌렸다고 알림
> 6) P -> M: P가 M한테 현재 시간을 물어봄
> 7) M: 현재 시간 구함
> 8) M -> P: M이 P한테 현재 시간을 알려줌
> 9) P -> V: P가 V한테 현재 시간을 버튼 밑에 그리라고 시킴
> 10) V: 버튼 밑에 현재 시간을 그림

> 요약: 일은 Model이 하고 화면은 View가 그림. Presenter는 둘을 이어줌.

---
&reference   
- [todoMVP - google architecture sample](https://github.com/android/architecture-samples/tree/todo-mvp)   
- [site1](https://beomy.tistory.com/43)
- [site2](https://awesometic.tistory.com/32?category=1046310)
