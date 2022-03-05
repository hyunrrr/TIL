## 두 개의 List를 Map으로 압축하기

### 학습동기
- 두 개의 List를 하나는 key, 하나는 value인 Map으로 압축하고 싶음
- 반복문을 이용할수도 있지만 더 좋은 방법은 없을까?

### 학습내용
- IntStream을 사용해 구현할 수 있음

```java
private static Map<K, V> zipToMap (
List<K> keys, List<V> values) {
    return IntStream.range(0, keys.size())
        .boxed()
        .collect(Collectors.toMap(
        keys::get, values::get));
}
```

### 결론
- IntStream을 잘 이용하면 반복문을 좀 더 간결하게 표현할 수 있다.

### 출처
https://stackoverflow.com/questions/1839668/what-is-the-best-way-to-combine-two-lists-into-a-map-java