# 📚 학습한 내용

## 1. 데이터 바인딩 (Data Binding)

XML 레이아웃 파일과 ViewModel 또는 데이터 소스를 직접 바인딩할 수 있는 기능을 학습.

데이터 바인딩을 통해 findViewById 호출을 대체하여 UI 코드를 간결하게 유지할 수 있음을 학습.

예: XML에서 @{} 표현식을 사용하여 데이터를 레이아웃과 바인딩.

-----------
## 2. MVVM 아키텍처

MVC를 대체 즉, 컨트롤러 역할의 규모가 크면 문제점이 있음. 뷰와 밀접한 컨트롤러 코드를 레이아웃 파일로 옮길 수 있는 MVVM 아키텍처를 학습.

MVVM의 ViewModel VS Jetpack ViewModel
 - 이 둘은 같은 것이 아니고, 젯펙의 뷰모델은 액티비티나 프래그먼트의 생명주기에 걸쳐 데이터를 유지하고 관리하는 클래스.
 - MVVM의 뷰모델은 개념적인 아키텍처의 일부분을 말한다. 따라서 뷰모델은 젯펙 뷰모델 클래스로 구현할 수 있고, 사용하지 않고도 구현 가능.

이 프로젝트에서는 Jetpack ViewModel을 사용하지 않고, LiveData와 비슷한 관찰 가능한 데이터 즉 뷰모델에서 데이터 바인딩의 Observable 인터페이스를 구현하여 관찰하도록 만들 수 있음을 학습. 

여기서는 BaseObservable 클래스를 사용. (대신에 LiveData를 사용해도 됨)

---
## 3. Asset 사용법

assets 폴더에 파일을 추가하고, 앱 내에서 해당 파일을 읽어오는 방법을 학습.

예: 텍스트 파일이나 리소스 파일을 동적으로 로드하여 UI에 반영. 

여기서는 오디오 파일 에셋 폴더에 추가하고 읽어 옴

---
## 4. 단위 테스트

JUnit과 Mockito를 사용하여 ViewModel의 단위 테스트를 진행.

---
## 5. 오디오 재생

안드로이드 오디오 API를 쉽게 사용하도록 해주는 도구인 SoundPool 클래스에 대해 학습.

---
## 6. 스타일과 테마

스타일은 위젯에 적용할 수 있는 속성들의 집합으로, 반복되는 속성을 재사용할 수 있다는 것을 배움.

스타일 간 상속을 통해 공통 속성을 재사용하는 방법을 학습.

테마는 앱 전반에 적용되는 스타일의 집합으로, 스타일의 단점인 위젯마다 적용해야하는 것을 보완 해줌.

테마 속성을 오버라이드하거나, 적합한 테마를 선택하는 방법을 배움.

여기서는 부모 테마로 AppCompat을 사용

---
## 7. Drawable

형태(shape): 원, 사각형 등 기본적인 도형 생성.

상태 리스트(State List): 버튼의 눌림 상태와 기본 상태 등 상태에 따라 UI를 변경.

레이어 리스트(Layer List): 여러 Drawable을 겹쳐서 복합적인 디자인 구현.

버튼의 배경 이미지가 크기 변화에 따라 왜곡되지 않도록 9-패치 이미지를 사용하는 방법을 학습.

9-패치를 통해 확장 될 부분을 지정. (이미지의 위쪽과 왼쪽 경계는 이미지가 확장 가능한 영역, 오른쪽과 아래쪽은 콘텐츠가 그려지는 영역.)