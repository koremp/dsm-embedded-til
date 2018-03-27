0325_Assignment

이전에
    콜백이 무엇인가?
    
    클래스 A는 클래스 B를 호출하여 스레드에서 수행 된 작업을 얻습니다. 스레드가 작업을 완료하면 클래스 A에 콜백을 알리고 결과를 제공합니다. 따라서 투표 나 기타 필요가 없습니다. 가능한 한 빨리 결과를 얻을 수 있습니다.

    Android 콜백에서는 f.e. 활동과 단편 사이. 프래그먼트가 모듈화되어야하므로 프래그먼트에서 콜백을 정의하여 액티비티의 메소드를 호출 할 수 있습니다.

    https://stackoverflow.com/questions/18054720/what-is-callback-in-android

Activity lifecycle

시스템이 새 액티비티 인스턴스를 생성하면, 각각의 콜백 메서드는 액티비티 상태를 한 단계 상향 이동합니다.
사용자가 액티비티를 나가면, 시스템은 액티비티를 해체하기 위해 액티비티 상태를 피라미드에서 하향 이동하는 다른 메서드를 호출합니다.

액티비티 시작
    모든 Activity의 생성시 onCreate() 메서드를 호출하여 매번 Activity의 새 인스턴스를 생성합니다.

    액티비티의 전체 수명 주기 동안 한 번만 발생하는 기본 애플리케이션 시작 논리를 수행하도록 onCreate() 메서드를 구현해야 합니다. 예를 들어 onCreate()의 구현은 사용자 인터페이스를 정의해야 하며, 몇몇 클래스 범위의 변수를 인스턴스화해야 할 수 있습니다.

    onCreate()가 실행을 마치면 시스템은 onStart() 및 onResume() 메서드를 연달아 호출합니다. 액티비티가 생성됨(Created) 또는 시작됨(Started) 상태에서 머무르는 경우는 없습니다. 엄밀히 말하면 onStart()가 호출되면 액티비티가 사용자에게 보이지만, onResume()이 바로 뒤따르고, 어떠한 상황(예: 전화가 오거나, 사용자가 다른 액티비티로 전환하거나, 기기 화면이 꺼진 경우)이 발생하기 전까지는 액티비티가 재개됨(Resumed) 상태로 유지됩니다.

    https://developer.android.com/training/basics/activity-lifecycle/starting.html?hl=ko#Create


액티비티 일시정지 및 재개
    일시정지
    액티비티가 보이지 않으면 애니메이션 또는 CPU 소비를 야기할 수 있는 기타 지속적인 작업을 정지
    저장되지 않은 변경 내용 커밋.
    브로드캐스트 수신기와 같은 시스템 리소스, GPS와 같은 센서에 대한 핸들 또는 액티비티가 일지정지된 동안 배터리 수명에 영향을 미칠 수 있으며 사용자가 필요로 하지 않는 모든 리소스 해제
    재개
    액티비티가 전면에 표시될 때마다 시스템이 이 메서드를 호출
    https://developer.android.com/training/basics/activity-lifecycle/pausing.html?hl=ko

액티비티 정지 및 재시작
    onStop, onRestart, onStart, onResume
    정지
    데이터베이스에 정보를 쓰는 작업과 같이 규모가 크고 CPU를 많이 사용하는 종료 작업을 수행하는 경우 onStop()을 사용
    시작/재시작
    액티비티가 보이게 될 때마다 발생
    

액티비티 재생성
    onSavedInstance, onCreate, onRestoreInstanceState
    EditText 위젯 내 텍스트 또는 ListView의 스크롤 위치와 같은 액티비티의 뷰 계층 구조에 대한 정보를 저장
    getInt, putInt
    https://developer.android.com/training/basics/activity-lifecycle/recreating.html?hl=ko


URL
1. https://developer.android.com/guide/components/activities.html?hl=ko
2. https://developer.android.com/training/basics/activity-lifecycle/index.html?hl=ko