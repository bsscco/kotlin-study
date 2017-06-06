# 안드로이드의 MVC
- View+Controller(Activity/Fragment)
	- 액티비티(프래그먼트)가 View의 역할과 Controller 역할을 동시에 했다.
- Model
  - UI의 상태를 가지고 있고, 상태를 갱신하는 비지니스 로직도 가지고 있는 클래스
	
# 일반적인 MVC
- Model
	- 안드로이드 MVC의 M과 같다.
- View(Activity/Fragment)
	- 받은 데이터로 렌더링에 집중한다. 다른 책임은 지지 않는다.
- Controller
	- V에서 발생하는 이벤트에 따라 M에 알리고, 갱신된 M 데이터를 V에 알리는 클래스. 액티비티(프래그먼트)로부터 C의 역할을 뺃어옴.
 
# 나아갈 MVP
- Model
	- MVC의 M과 같다.
- View(Activity/Fragment)
	- MVC의 V와 같다.
- Presenter
	- MVC의 C와 같다. 
- 그럼 MVC랑 뭐가 다른가?
	- MVC의 V와 C는 다수:1로 대응된다. MVP의 V와 P는 1:1로 대응된다. MVP는 MVC의 C에 집중되어있는 많은 코드들을 MVP의 여러 개의 P들로 나누었다. 이로 인해 더 testable하게, maintainable하게 된다.
