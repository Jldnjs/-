# 24/01/18 🐔

## static
  : 객체는 서로 다른 상태를 갖는다. 그래서 인스턴스 변수 사용하는데, static 변수는 같은 상태를 갖는 경우 사용한다.

## final 필드
  : 더이상 수정 불가능한 필드

## final 클래스
  : 더이상 상속 불가능한 클래스.

## final 메소드
  : 오버라이딩 금지하는 메소드.

## Abstract(추상)
- 추상 메서드
  : 구현부x / 구체적 행위를 하지 않고, 형태만 가지고 있다.
  구현부가 없는 이유는 어차피 상속받는 클래스에서 각자 다른 값 입력하기 때문에 쓰레기 값을 생성하지 않는다.
  그래서 인스턴스 생성을 막기 위함이다.

  => 구현부가 없는 메서드는 실행하면 오류가 나기 때문에 추상메서드가 포함된 클래스 앞에는 abstract로 명시해둔다.
  `추상클래스는 인스턴스 생성이 불가능하다`
  `추상메서드를 포함한 클래스는 추상클래스이며 abstract로 명시해둬야한다.`

## 클래스 형변환
- 부모 클래스가 자식 클래스를 가리키고 있는 상황에서, 부모클래스 형태의 인스턴스가 자식 인스턴스까지 참조하고자 할 때 명시적으로 형변환 하는 것.
```java
class Super{
  public void a(){
    System.out.println("Super : a()");
}

class Sub extends Super{
  public void a(){
    System.out.println("Sub : a()");
  }
  public void b(){
    System.out.println("Sub : b()");
  }
}

public class Casting{
  public static void main(String args[]){
    Super s3 = new Sub(); //-> 묵시적 형변환
    s3.a();
    //s3.b(); // s3은 b를 참조할 수 없다.

    Sub sub = (Sub)s3;
    sub.b(); //형변환으로 b참조 가능
  }
}

```

## 인터페이스
 : 추상 자료형.
 abstract처럼 재 정의 하지 않으면 오류난다. => 오버라이딩 강제성

> 특징
>   > 다중상속가능
>   > 추상메서드와 상수만 사용가능
>   > 생성자 사용 불가
>   > 메서드 오버라이딩 필수

## 생성자
 :  객체 생성될 때 호출되는 메서드

## 메소드 오버로딩
  : 특정 클래스 안에서 파라미터가 다른 동일한 이름의 메서드 선언

### toString

## Object
 : 모든 api(application programming interface)의 최상위 클래스
 ### API
  : 응용프로그램에서 사용할 수 있도록 운영체제나 프로그래밍 언어가 제공하는 기능을 제어할 수 있게 만든 인터페이스를 뜻한다.
