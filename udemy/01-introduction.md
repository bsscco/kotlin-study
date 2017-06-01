# 소개
### 뭐니?
- JVM에서 돌아감. -> 100% 자바와 호환
- Null safety
- 현대 언어들의 기능을 잘 갖추고 있어서 Lambda나 Stream을 쓸 필요가 없다.

### 뭐랑 비슷하다.
- Swift와 비슷하다.

# 준비
### 플러그인 설치
- AndroidStudio-Preferences-Plugins-Kotlin 설치
- Kotlin Extentions for Android는 deprecated 됨.

### 의존성 추가
- Tools-Kotlin-Configure Kotlin in Project-Android with Gradle-OK 클릭
- Sync Now를 클릭

### .java to .kt
- Code-Convert Java File to Kotlin File 

# 기본 문법
### Basic
- 기본 타입 없이 전부 객체
- val / var
- 타입 유추
	- 정수 유추 기본 타입은 Int
	- 실수 유추 기본 타입은 Double
- 함수 축약
- 지역 함수
- 중위 표기법
	- ```fun Int.plus(x: Int) = this + x```는 ```1.plus(x)```로  쓸 수 있음.
	- ```infix fun Int.plus(x: Int) = this + x```는 ``1 plus x```로 쓸 수 있음. 단, 인자가 1개일 때만 사용 가능.

### NULL
- Kotlin은 기본이 NonNull
- null을 넣으려면 ```var a: Int?```와 같이 선언

### String
- string template
	- ```"Name $name length = ${name.length}"```

### Any
- Java의 Object
- is와 조합
	```kotlin
	if(a is String) {
		println(a.length)
	}
	```
- when과 조합
	```kotlin
	when(a) {
		1 -> println("Number")
		is String -> println("String")
		else -> println("Unknown")
	}
	```

### Loop
- ```for(s in arr)```
- ```for(x in 1..5)```

### Lambda
- ```v.setOnClickListener { it.alpha = 0.5f }``` 단, 인자가 1개일 때만 it 사용 가능.

### Stream
- ```list.filter { it > 5 }.map { println(it * 2) }```
