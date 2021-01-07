Android Develop Lifecycle
=========================
![activity lifecycle](/image/activity-lifecycle.png)

onCreate()
- Activity가 처음 생성될 때 호출됨
- 매개변수인 savedInstanceState를 통해 이전 상태를 불러옴
- Activity에 필요한 구성 요소들을 초기화
- UI 레이아웃 초기화
- 저장되었던 데이터에 의해 화면을 이전 상태로 복구

onRestart()
- Activity가 중단되었다가 다시 시작되기 전 호출됨

onStart()
- Activity가 화면에 보이기 바로 직전에 호출됨

onResume()
- Activity가 사용자와 상호작용을 하기 바로 직전에 호출됨
- 호출된 후 실질적으로 사용자가 사용 가능한 Activity가 실행됨

onPause()
- Activity가 다른 Activity로 가려져 화면에서 사라지기 시작할 때 호출됨
- BroadcastReceiver, 센서 처리, 활동이 일시중지되어 사용자에게 필요하지 않은 리소스 등을 해제할 수 있음
- 해당 구간은 매우 짧기 때문에 [안드로이드 가이드](https://developer.android.com/guide?hl=ko)에서는   
  사용자의 데이터 저장 및 네트워크 호출, 데이터베이스의 트랜젝션 처리 등을 수행하지 말 것을 권장
> 간단한 예제   
> : 앱 사용 도중 전화가 와서 전화를 받고 다시 앱으로 돌아오는 시나리오에서 Activity의 동작   
>
> Activity 실행 도중 인터럽트 발생 시 onPause() 호출   
> → 다시 Activity로 돌아오면 onResume() 호출

onStop()
- Activity가 더 이상 보이지 않을 때(Activity 종료 or 다른 Activity가 화면을 가린 경우)에 호출됨
- 해당 구간에서는 Activity Object 메모리만 남아있게 됨
- 해당 구간에 들어오면 바로 onSaveInstanceState()가 실행되어 데이터를 key-value 형태로 저장   
  → onCreate()에서 다시 복원할 수 있도록 함

onDestroy()
- Activity가 완전히 소멸될 때 호출됨
- 사용자가 종료 or 시스템에서 메모리 절약을 위해 강제적으로 종료

![fragment lifecycle](/image/fragment-lifecycle.png)

Fragment는 Activity 내에 존재하며   
Fragment를 Activity에 생성하여 하나의 Activity에 여러 개의 화면을 구성할 수 있도록 함

onAttach()
- Fragment가 Activity에 연결될 때 호출됨

onCreate()
- Fragment가 처음 생성될 때 호출됨
- 리소스들 초기화
- 생성 시 넘겨받은 값들이 있다면 해당 구간에서 변수에 할당
- 해당 구간에서는 UI에 대한 작업 불가능

onCreateView()
- Fragment의 layout을 inflate하여 View 객체를 얻을 수 있음
- View와 관련된 버튼이나 TextView와 같은 구성요소들 초기화 가능

onActivityCreated()
- Activity에서 Fragment가 모두 생성된 후에 호출됨
- 해당 구간에서부터 UI에 관련된 View를 변경하는 작업 가능

onStart()
- Fragment가 화면에 보이기 바로 직전에 호출됨

onResume()
- Fragment가 사용자와 상호작용을 하기 바로 직전에 호출됨

onPause()
- Fragment or Activity의 교체 등으로 인해 다른 Fragment가 화면을 가리게 되어 기존 Fragment가 사라지기 시작할 때 호출됨
- 사용자와의 상호작용 중지, 기존 layout은 back stack으로 들어감

onDestroyView()
- Fragment의 View들의 리소스가 해제됨

onDestroy()
- Fragment가 완전히 소멸될 때 호출됨

onDetach()
- Fragment가 Activity와 연결이 끊기기 직전에 호출됨

&reference
- [site](https://re-build.tistory.com/4)
