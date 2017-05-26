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
- ```kotlin
	while (i < args.size)
		println(args[i++])
	```
- do...while문 또한 Java와 같이 잘 동작한다.

### Use for-loop.kt
- ```kotlin
	for (arg in args)
		println(arg)

	// or

	for (i in args.indices)
			println(args[i])

	```
