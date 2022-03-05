## TreeSet을 사용하려면 compareTo를 구현하자

### 학습동기
```java
Set<LottoNumber> numbers = new TreeSet<>();
```
을 사용하니 런타임 에러가 발생

### 학습내용
- Custom object를 정렬하기 위해선 compareTo()를 오버라이드해 sorting logic을 제공해야 됨

### 결론
TreeSet을 사용하려면
```java
public class LottoNumber implements Comparable<LottoNumber> {
...
    @Override
    public int compareTo(LottoNumber other) {
        return this.number - other.number;
    }
}
```
를 구현해 사용하자

### 출처
https://www.thejavaprogrammer.com/cannot-be-cast-to-java-lang-comparable/