# LiveData
LiveData는 우리는 Activity이나 Fragment으로부터 ViewModel의 데이터를 observe하는 코드를 작성할 수 있다.
그리고 이러한 데이터에 대한 change가 발생할 경우 LiveData를 사용하여 Activity이나 Fragment을 자동으로 업데이트하는 코드를 작성할 수 있다.
LiveData는 라이프사이클 인식 관측 가능한 데이터 홀더 클래스다. 안드로이드에서 우리는 라이프사이클이 있는 3가지 앱 구성요소를 가지고 있다. Activity, Fragment
그리고 Service. 따라서 Activity, Fragment 및 Service를 LiveData 객체의 관찰자로 사용할 수 있다. LiveData는 활성 라이프사이클 상태에서만 관찰자를 업데이트한다.
그렇다면, 실시간 데이터를 사용할 때의 이점은 무엇인가? LiveData는 앱 데이터가 변경되면 UI를 자동으로 업데이트한다. 따라서 실시간 데이터를 사용하면 항상 최신 데이터를 가질 수 있다. 
실시간 데이터에서는 라이프사이클을 수동으로 처리하기 위해 코드를 작성할 필요가 없다. 라이브 데이터는 라이프사이클의 상태 변화를 인식하기 때문에 관련 라이프사이클이 파괴될 때 스스로 정리한다.
따라서 destroyed된 Activity이나 Fragment의 결과로 메모리 누수나 충돌은 일어나지 않을 것이다. 우리는 또한 라이브 데이터를 사용하여 앱의 다른 구성 요소들 간에 앱의 서비스를 공유할 수 있다.
#
## MutableLiveData
MutableLiveData와 LiveData의 차이점은 무엇인가? LiveData 개체의 데이터는 읽기만 가능하다.우리는 그 데이터를 갱신할 수 없다.
MutableLive 데이터 클래스는 LiveData 클래스의 하위 클래스다. Mutable LiveData 개체를 사용하면 데이터를 변경할 수 있다.