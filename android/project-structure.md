프로젝트 구조
=============

안드로이드 스튜디오 프로젝트 구조
- manifest, java, res, Gradle Scripts

#### 1. manifest
해당 앱의 전반적인 정보를 담고 있는 파일(명함, 인적사항같은 것)
- 모든 앱은 manifest.xml이 있어야 함
- java package 이름으로 어플리케이션내에 유일해야 함.
- 기술되는 내용은 어플리케이션의 컴포넌트들
> ex) 액티비티, 서비스, 브로드캐스트 등
- 다른 어플리케이션과의 작업을 할 때 접근에 대한 권한 등을 선언(제한 or 허용)
- Instrumentation classes의 리스트들 : 개발 및 테스트에 사용
- 최소 안드로이드 API Level 정의
- 라이브러리 리스트

#### 2. java
MainActivity.java 파일이 존재하는데 어플리케이션을 실행하면 MainActivity를 동작시키고 layout 파일을 호출하게 됨

#### 3. res
- 리소스 파일
- Activity의 layout을 정의
- activity_main.xml에 textView에 친숙한 HelloWorld!!를 확인 할 수 있음
- 안드로이드 프로그래밍은 GUI를 사용하게 되기 때문에 layout system을 사용

#### 4. gradle
- 앱의 빌드와 컴파일에 대한 정보
- 이클립스는maven을 주로 사용하지만 안드로이드 스튜디오는 gradle을 사용
---
&reference   
- [site](https://m.blog.naver.com/PostView.nhn?blogId=khrock89&logNo=220918924049&proxyReferer=https:%2F%2Fwww.google.com%2F)   
- [android developer](https://developer.android.com/training/basics/firstapp/creating-project.html)   
- [manifest intro](https://developer.android.com/guide/topics/manifest/manifest-intro.html)
