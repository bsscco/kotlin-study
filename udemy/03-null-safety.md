### Java vs Kotlin
- ```void func(@NotNull String a, @Nullable String b)```
- ```fun func(a: String, b: String?)```

### Nullable 선언 시 주의사항
- nullable을 선언할 땐 타입을 명시해야 null이 아닌 값을 대입할 때 오류가 나지 않는다. ```var temp: String? = null```

### 팁
- 깊은 멤버 데이터를 대입할 때 null-safety하게 구현하는 법
	- ```obj?.a?.b?.c?.name ?: "defalut value"``` elvis operator를 사용한다.

- 선 null 체크가 필요한 로직은 if문 대신에 ?.let{}으로 구현한다.
	- ```item?.let { println(it) }```

- list엔 filterNotNull()이라는 메소드가 있다.
