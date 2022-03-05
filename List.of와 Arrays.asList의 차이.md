## List.of와 Arrays.asList의 차이

### **학습동기**
많이 사용하는 List 자료구조, 크기가 고정된 배열을 만들어주는 Arrays.asList를 종종 사용했는데, 자바9에 List.of가 추가되었다고 한다. 둘의 차이가 궁금해 찾아봄

### **학습내용**
1. Arrays.asList는 mutable list를, List.of는 immutable list를 반환
2. Arrays.asList는 null원소를 허용, List.of에선 안됨
3. contains(null)의 결과가 다름, Arrays.asList로 만들어진 얘는 true/false, List.of는 NullPointerException
4. 배열을 인자로 넘겨줬을때, Arrays.asList의 결과는 배열값이 바뀌면 따라바뀜, List.of는 안바뀜

### **결론**
불변이 대세인거 같으니 List.of쓰자

### **출처**
https://stackoverflow.com/questions/46579074/what-is-the-difference-between-list-of-and-arrays-aslist