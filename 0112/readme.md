# 23/01/12 (금) :beer:

## :repeat:
### 1. System 개발 절차
  요구사항 정의 -> 분석 -> 설계 -> 구현
### 2. Java 개발 환경
  .java파일 -> .class 로 변환 -> Java Platform(JDK/SDK/..) -> run

### 3. Language 기본

<hr>

## UML(Unified Modeling Language)
  : 표준화된 범용 모델링 언어
  - 서비스에 들어가는 정보와 복잡한 구조들을 단순하게 보여줄 때 주로 사용됨.

## Java 코딩 컨벤션 
### 카멜 케이스(Camel Case)
  : 첫 문자는 소문자로 시작하고, 이후 연결되는 단어의 첫 문자는 대문자로 잇는 표기법
  
```java
int camelCase;
```
 - 변수명 정의할 때 사용

### 파스칼 케이스(Pascal Case)
  : 첫 문자 모두 대문자로 시작하는 표기법.

```java
int PascalCase;
```
- 클래스명 정의할 때 사용

### 스네이크 표기법(Snake Case)
  : 단어 사이를 _(언더바)로 잇는 표기법.
  
```java
int snake_case;
static final boolean START_FLAG;
```
- 상수명 정의할 때 사용

### 헝가리안 표기법(Hungarian Notation)
  : 접두어에 자료형표기.

```java
String strName;
```

### 케밥 케이스(Kebab case)
  : 모든 문자를 소문자로 표현하며 단어와 단어 사이에 대시문자(-)로 구분하여 표기.
  
```java
int kebab-case;
```
- 스프링의 yml파일, url 주소표기에 사용.

` Java의 코딩컨벤션을 이해하면 System.out.println() 문의 System 이 클래스이고, .out과 .println이 System에 속해있는 메서드라는 것 유추 가능.
 Math.random() 에서도 Math == class ` 

## break / continue

- break
  : 반복문 빠져나가는 명령어.
- continue
  : 하부 수행 중지 후 재실행 하는 명령어.

## Array
: 같은 데이터 타입의 묶음

```java
//int[] intArray;
//int intArray[];

//int[] intArray = new int[9];
//int[] intArray = {1,2,3,4,5,6,7,8,9};
//int[] intArray = new int[]{1,2,3,4,5,6,7,8,9};
```

### 배열의 배열
  : 자바는 다중배열이 아니라 하나의 배열속에 배열이 있는 개념이다.

```java
int[][] c = new int[2][3];

System.out.println(c.length); // 2
System.out.println(c[0].length); // 3
```
>  생성 순서
> : c 배열 생성 -> 2개의 공간이 있는 배열 생성 -> 각각의 칸에 length 3짜리 배열 생성
>
>  => 그래서 배열 c의 length는 2이다. 배열 c[0] 의 length는 3, c[1] 의 length3도 3.

