### 생성자
- 별도 구현 내용이 없다면 중괄호도 생략 가능하다. ```class Foo```
- 코틀린 프라이머리 생성자는 class 이름 끝에 괄호로 나타낼 수 있다. ```class Foo(val a: Int, var b: Int) {...}```
- 다중 생성자가 있을 때 모든 생성자의 인자를 프라이머리 생성자에서 선언해주면 클래스에서 접근할 수 있다.
	```Kotlin
	class Foo(val a: Int, val b: Int) { 

		constructor(val a:Int) : this(a, b) {
			...
		}
	}
	```
- 생성자에서 디폴트값 사용하기 ```class Foo(val a: Int = 0)```
- private 생성자 ```class Foo private constructor()```

### 함수 재정의
- Kotlin은 기본이 final 클래스, 함수. open 키워드를 사용해야 재정의 가능 (interface는 open 필요 없음)
- abstract 키워드는 val멤버변수와 멤버함수 모두에게 적용할 수 있다. val멤버변수는 상속 후 재정의 할 수 있다.

### 인터페이스
- 인터페이스는 멤버변수와 멤버함수 모두 가질 수 있다. 단, 멤버변수는 상속할 때 정의할 수 있고, 멤버함수는 인터페이스에서 정의할 수 있다.
