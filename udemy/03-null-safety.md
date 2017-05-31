### Java vs Kotlin
- ```void func(@NotNull String a, @Nullable String b)```
- ```fun func(a: String, b: String?)```

### Null 주의사항
- nullable을 초기화할 땐 타입을 명시해야 null이 아닌 값을 대입할 때 오류가 나지 않는다. ```var temp: String? = null```

### 팁
- 깊은 멤버 데이터에 접근할 때 null-safety하게 구현하는 법
  - ```obj?.a?.b?.c?.name ?: ""```
