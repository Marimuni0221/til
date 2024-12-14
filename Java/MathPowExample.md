## Javaにおけるべき乗

### Javaでは、べき乗を計算するために Math.pow メソッドを使用
```java
Math.pow(base, exponent);
```

### したがって、((a + b) * c)^2 を正しく計算するには次のようになる
```java
Math.pow(((a + b) * c), 2);
```

### もし整数で結果を求めたい場合は、int にキャストする必要がある
```java
(int) Math.pow(((a + b) * c), 2);
```