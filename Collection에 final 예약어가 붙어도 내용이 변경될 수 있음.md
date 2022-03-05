## Collection에 final 예약어가 붙어도 내용이 변경될 수 있음

### **학습동기**
final만 붙이고 return하면 외부에서 안의 내용은 변경될 수 있다고 함

### **학습내용**
```java
private final List<Integer> numbers;
```
위의 final이 보장해 주는것은 numbers의 모든 원소가 불변이라는 것이 아닌 "numbers가 참조하는 객체는 변하지 않음"이다.
따라서 getter로 numbers을 바로 리턴해주면 외부에서 numbers의 원소를 바꿀 수 있음!

### **결론**
getter를 사용할 경우 Collections.unmodifiable~ 를 사용해 원소의 불변도 보장하자
```java
public List<Integer> getNumbers() {
    return Collections.unmodifiableList(this.numbers);
}
```