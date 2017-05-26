# Hello, world!

### Simplest version.kt
- 세미콜론(;)은 선택사항
- 반환값이 없을 땐 Unit을 리턴하거나 생략 가능

### Reading a name from the command line.kt
- string template ```"Hello, ${args[0]}!"```

### Reading many names from the command line.kt
- loop ```for (name in args)```

### A multi-language Hello.kt
- if expression ```val language = if (args.size == 0) "EN" else args[0]```
- when expression
	```kotlin
	println(when (language) {
			"EN" -> "Hello!"
			"FR" -> "Salut!"
			"IT" -> "Ciao!"
			else -> "Sorry, I can't greet you in $language yet"
	})
	```
### An object-oriented Hello.kt
- class definition and primary constructor
	```kotlin
	class Greeter(val name: String) {
	}
	```
- 객체를 생성할 때 new 키워드가 필요하지 않다. ```Greeter(args[0]).greet()```



# Basic syntax wolk-through

### Use a conditional expression.kt
- if expression ```fun max(a: Int, b: Int) = if (a > b) a else b```
- if expression 덕에 ternary operator는 더 이상 필요하지 않다.

### Null-checks.kt
- nullable이 되려면 퀘스찬마크(?)를 반드시 붙여줘야 한다. ```fun parseInt(str: String): Int? {``` 

### is-checks and smart-casts.kt
- is operation은 Java의 instanceof와 같다.
- 만약 is-checked 변수가 있다면 명시적 casting을 할 필요가 없다.
	```kotlin
	fun getStringLength(obj: Any): Int? {
		if (obj is String)
				return obj.length // no cast to String is needed
		return null
	}
	```

### Use a while-loop.kt
- while
	```kotlin
	while (i < args.size)
		println(args[i++])
	```
- do...while문 또한 Java와 같이 잘 동작한다.

### Use for-loop.kt
- for 
	```kotlin
	for (arg in args)
		println(arg)

	// or

	for (i in args.indices)
			println(args[i])

	```

### Use ranges and in.kt
- if in ```if (x in 1..y - 1)```
- for in ```for (a in array)```
- range ```for (a in 1..5)```

### Use when.kt
- when
	```kotlin
	when (obj) {
        1 -> println("One")
        "Hello" -> println("Greeting")
        is Long -> println("Long")
        !is String -> println("Not a string")
        else -> println("Unknown")
    }
	```



# Destructuring declarations

### Destructuring declarations.kt
- [문서](http://kotlinlang.org/docs/reference/multi-declarations.html#destructuring-declarations)
- 때때로 몇 개의 변수 안으로 객체를 파괴해 넣는 것은 편리합니다. 이것을 destructuring declarations라고 부릅니다. ```val (name, age) = person```
- 그 밖에 for-loop에서도 돌아갑니다. ```for ((a, b) in collection) { ... }```
- 위 코드는 아래와 같이 컴파일됩니다.
	```kotlin
	val name = person.component1()
	val age = person.component2()
	```
- componentN() 함수를 정의할 땐 operator 키워드가 필요합니다.
- 이것은 두 가지 이상의 값을 리턴할 때 유용합니다.
	```kotlin
	data class Result(val result: Int, val status: Status)
	fun function(...): Result {
		// computations

		return Result(result, status)
	}

	// Now, to use this function:
	val (result, status) = function(...)
	// 우리는 그 밖에 standard class인 Pair를 사용할 수도 있습니다.
	```
- data class는 자동으로 componentN()를 생성해줍니다.
- map-loop에 사용하기
	```kotlin
	for ((key, value) in map) {
	   // do something with the key and the value
	}
	```
- destructuring declarations가 필요하지 않을 때는 underscore를 사용합니다. ```val (_, status) = getResult()```
- 두 가지 파라메터와 destructuring 페어의 차이점을 알아두세요.
	```kotlin
	{ a -> ... } // one parameter
	{ a, b -> ... } // two parameters
	{ (a, b) -> ... } // a destructured pair
	{ (a, b), c -> ... } // a destructured pair and another parameter
	```
	
### Data classes.kt
- [문서](http://kotlinlang.org/docs/reference/data-classes.html#data-classes)
