## List에 add하니 UnsupportedOperationException가 발생

### 학습동기
- List에 add를 하니 UnsupportedOperationException가 발생

### 학습내용
- Arrays.asList로 만들어진 배열은 우리가 흔히 사용하는 ArrayList를 반환하는 것이 아님. 이는 add와 remove와 같은 변환과 관련된 메서드를 지원하지 않음.
- 따라서 UnsupportedOperationException와 같은 익셉션이 발생하는 것

### 결론
- new ArrayList<>(Arrays.asList()) 를 사용하자

### 출처
https://stackoverflow.com/questions/5755477/java-list-add-unsupportedoperationexception