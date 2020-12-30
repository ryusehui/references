PATTERN MVC
===========
![MVC pattern](/image/MVC.png)

## 모델-뷰-컨트롤러

#### 1. 구조
- Model: 앱에서 사용되는 데이터와 그 데이터를 처리
- View: 사용자에게 보여지는 UI
- Controller: 사용자의 입력을 받고 처리하는 부분

#### 2. 동작
1) 사용자의 action이 controller에 들어옴
2) controller는 사용자의 action을 확인하고 model을 업데이트함
3) controller는 model을 나타내줄 view 선택
4) view는 model을 이용하여 화면을 나타냄   
> 참고) MVC에서 view가 업데이트 되는 방법
>- view가 model을 이용하여 직접 업데이트
>- model에서 view에게 notify하여 업데이트
>- view가 polling으로 주기적으로 model의 변경을 감지하여 업데이트

#### 3. 특징
- controller는 view를 선택할 뿐 직접 업데이트하지 않음(view는 controller를 알지 못함)
- controller는 여러개의 view를 선택할 수 있는 1:n 구조

#### 4. 장단점
- 장점: 가장 단순한 패턴
- 단점: view와 model 사이의 의존성이 높아 앱이 커질수록 복잡해지고 유지보수가 어려워질 수 있음
---
&reference    
- [site](https://beomy.tistory.com/43)
