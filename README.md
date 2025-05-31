# JAVA_String  

## ✅ 문자열(String)이란? 문자들의 나열. 문자 하나 이상을 연결한 텍스트 데이터.  

## 문자열 기능  
```
String s = "I like Java and Python and c.";
System.out.println(s);

// 문자열의 길이 출력
System.out.println(s.length()); // 29

// 대소문자 변환 출력
System.out.println(s.toUpperCase()); // 대문자로 변경
System.out.println(s.toLowerCase()); // 소문자로 변경

// 포함관계
System.out.println(s.contains("Java")); // Java 가 있다면 true 없다면 false
System.out.println(s.contains("C#"));
System.out.println(s.indexOf("Java")); // Java 라는 문자의 위치정보
System.out.println(s.indexOf("C#")); // 포함되지 않는다면 -1
System.out.println(s.indexOf("and")); // 처음으로 만나는 and의 위치정보
System.out.println(s.lastIndexOf("and")); // 마지막에 일치하는 and 의 위치정보
System.out.println(s.startsWith("I like")); // 이 문자열로 시작하면 true 아니면 false
System.out.println(s.endsWith(".")); // 이 문자열로 끝나면 true 아니면 false

//문자열 변환
System.out.println(s.replace("and" , ",")); // "and" 를 "," 로 변환
System.out.println(s.substring(7)); // 7번째 위치부터 시작 이전 내용은 삭제
System.out.println(s.substring(s.indexOf("Java"))); // Java의 위치값을 입력하여 그 위치부터 시작
// "Java" 가 시작하는 위치부터 "."이 시작하는 위치 바로 앞까지
System.out.println(s.substring(s.indexOf("Java"), s.indexOf("."))); // 시작위치부터 끝 위치 직전 까지

//공백제거
s = "    I like Java and Python and C.    ";
System.out.println(s.trim()); // 앞뒤 공백 제거

//문자열 결합
String s1 = "Java";
String s2 = "Python";
System.out.println(s1 + s2); // JavaPython
System.out.println(s1 +","+ s2); // Java,Python
System.out.println(s1.concat(","). concat(s2)); // Java,Python
```
## 문자열 비교  
```
String s1 = "Java";
String s2 = "Python";

System.out.println(s1.equals("Java")); // 문자열 내용이 같으면 true, 다르면 false
System.out.println(s2.equalsIgnoreCase("python")); // 대소문자 구문 없음

s1 = "1234";
s2 = "1234";
System.out.println(s1.equals(s2)); // true
System.out.println(s1 == s2); // true

s1 = new String("1234");
s2 = new String("1234");
System.out.println(s1.equals(s2)); // true
System.out.println(s1 == s2); // false
```
new String 의 s1, s2는 다른 메모리 위치에 있는 서로 다른 객체  
그래서 s1 == s2는 false (주소가 다름)  
"equals" = 문자 내용만 비교  
"==" = 주소(참조) 비교  
문자열 비교는 무조건 .equals()를 써야 정확  
