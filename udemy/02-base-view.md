### 팁
- ```유틸```은 static class 대신에 대상 class에 중위표기법으로 구현한다.
	- 중위표기법을 사용하면 static method를 사용하는 것에 비해 간결해지는 이점이 있다.
	- static method는 대상 인스턴스를 인자로 넣어주어야 작업이 가능하기 때문에 불편하기 때문이다.

- ```뷰 바인딩```은 Java에서는 ButterKnife로, Kotlin에서는 lazy문으로 구현한다.

- ```조건이 있는 대입식```은 when expression 또는 try~catch expression으로 구현한다.
	- when expession 안에서 어떤 케이스에도 걸리지 않으면 안전한 널 처리를 위해 elvis operator```?:```를 사용할 수 있다.

- static method는 companion syntax로 구현한다.
