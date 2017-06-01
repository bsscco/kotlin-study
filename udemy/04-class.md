### constructor
- 별도 구현 내용이 없다면 중괄호도 생략 가능하다. ```class Foo```
- primary constructor는 class 이름 끝에 괄호로 나타낼 수 있다. ```class Foo(val a: Int, var b: Int) {...}```
- multi-constructor가 있을 때 모든 constructor의 인자를 primary constructor에서 선언해주면 memeber attribute로 작용한다.
	```Kotlin
	class Foo(val a: Int, val b: Int) { 

		constructor(val a:Int) : this(a, b) {
			...
		}
	}
	```
- constructor에서 디폴트값 사용하기 ```class Foo(val a: Int = 0)```
- private constructor로 선언하기 ```class Foo private constructor()```

### function overriding
- Kotlin은 기본이 final class와 final method. open 키워드를 사용해야 overriding 가능 (interface는 open 필요 없음.)
- abstract 키워드는 val attribute와 method 모두에게 적용할 수 있다. val attribute는 상속 후 overriding 할 수 있다.

### interface
- interface는 attribute와 method 모두를 가질 수 있다. 단, attribute는 상속할 때만 정의할 수 있고, method는 interface에서 정의할 수 있다.
- attribute와 method는 open 키워드 없이도 상속받는 쪽에서 open으로 인식된다.

### multi-inheritance
- 다중 상속, 예를 들어 AAA class와 III interface를 상속하는 Inheri class가 있다고 할 때 Inheri는 AAA와 III의 겹치는 method 중 어떤 걸 사용할지 결정해야 한다.
	```kotlin
	open class AAA {
		open fun go() {
			...
		}
	}
	
	inteface III {
		fun go() {
			...
		}
	}
	
	class : AAA(), III {
		override fun go() {
			super<AAA>.go()
			super<III>.go()
		    }
	}
	```
