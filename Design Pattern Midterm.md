<h1>Design Pattern</h1>

<h1>강의 소개</h1>

<h2>디자인 패턴이란 무엇인가?</h2>

- 디자인 패턴이란?
  - 소프트웨어를 설계할 때 자주 발생하는 문제들에 대한 "재사용 가능한 해결책" - 크리스토퍼 알렉산더

<h2>디자인 패턴이 주는 이점</h2>

- 경험이 많은 소프트웨어 엔지니어들의 이 같은 해법을 사용
  - 공통 언어 역할을 하게 되어, 경험 많은 이들이 이 공통의 언어를 이용하면 그렇지 않을 경우보다 좀 더 효율적으로 협동 작업 가능
  - 불필요한 논쟁 시간 줄임
  - 디자인 해법에 대한 학습
  - 시스템의 안정성과 성능을 높일 수 있는 장점이 있다.

<h2>GoF 설계 패턴</h2>

- 생성 creational
  - 객체의 생성과 관련
    - 추상 팩토리 Abstract Factory
    - <span style="color:red">빌더 Builder</span>
    - 팩토리 메서드 Factory Method
    - 프로토타입 Prototype
    - <span style="color:red">싱글턴 Singleton</span>
- 구조 structural
  - 클래스나 객체들을 조합해 더 큰 구조로 만들 수 있게 해주는 패턴
    - 어댑터 Adapter
    - 브리지 Bridge
    - 컴퍼지트 Composite
    - 데커레이터 Decorator
    - 플라이웨이트 Flyweight
    - 프록시 Proxy
- 행위 behavioral
  - 객체들이 서로 소통하는 방법이나 어떤 태스크, 어떤 알고리즘을 어떤 객체에 할당하는 것이 좋을지를 정의
    - 책임 연쇄 Chain of Responsibility
    - 커맨드 Command
    - 인터프리터 Interpreter
    - 이터레이터 Iterator
    - 메멘토 Memento
    - 옵서버 Observer
    - 스테이트 State
    - <span style="color:red">스트래티지 Strategy</span>
- 이러한 패턴들을 사용하여 객체간의 효과적인 상호작용을 가능케 한다.

<br>

<h1>UML 모델링</h1>

<h3>클래스 다이어그램</h3>

- 설계 패턴의 <span style="color:red">정적인 구조 (클래스와 그들 간의 관계)</span> 표현

<h3>순차 다이어그램</h3>

- 설계 패턴의 <span style="color:red">행위</span>를 표현

<h3>UML</h3>

- 대표적인 시스템 모델링 언어

- UML에서의 클래스 표현
  - 클래스 이름 - 속성 - 연산 순으로..
- <span style="color:red">접근제어자</span>
  - public +
  - protected #
    - 상속 관계에 있는
  - package ~
    - 동일 패키지에 있는
  - private -
    - 해당 클래스로부터 생성된 객체들만
- 설계 단계의 클래스에서 초기값 설정도 가능함
- UML에서 static (정적) 연산을 위해 <span style="color:red">밑줄</span>로 표기

<h3><span style="color:red">관계</span></h3>

- 연관 association
  - 실선이나 화살표
- 일반화 generalization
  - 상속 관계, 속이 빈 화살표
- 집합 composition, aggregation
  - 합성, 집약
- 의존 dependency
  - 매우 짧은 시간, 점선 화살표
- 실체화 realization
  - 빈 삼각형, 점선

<h3>연관 관계</h3>

- 역할
- 연관 관계 이름
- 다중성
- 양방향, 단방향
  - 양방향 연관 관계
    - 화살표 X, 서로의 존재를 인지
  - 단방향 연관 관계
    - 한 쪽은 알지만 다른 쪽은 상대방의 존재를 모름

<h3>일반화</h3>

- 일반화는 "is a kind of" 관계

<h3>집합 관계</h3>

- <u>전체와 부분간의 관계</u>
- 집약 aggregation
  - <span style="color:red">전체를 나타내는 객체와 부분을 나타내는 개체의 라이프 타임이 <u>독립적</u></span>
  - <span style="color:red">부분을 나타내는 객체를 다른 객체와 공유 가능</span>
  - <span style="color:red">빈 마름모로 표시</span>
- 합성 composition
  - <span style="color:red">전체를 나타내는 객체에 부분을 나타내는 개체의 라이프 타임이 <u>종속적</u></span>
  - <span style="color:red">전체 객체가 사라지면 부분 객체도 사라짐</span>
  - <span style="color:red">채워진 마름모로 표시</span>
- ex)
  - 동아리가 없어지면 동아리에서 활동했던 학생들의 정보도 없어진다. -> composition으로 구현

<h3>의존 관계</h3>

- 한 클래스에서 다른 클래스를 사용하는 경우
  - <span style="color:red">클래스의 속성에서 참조</span>
  - <span style="color:red">연산의 인자로 참조</span>
  - <span style="color:red">메소드의 지역 개체로 참조</span>
- 연산의 인자나 메소드의 지역 개체로 참조
  - <span style="color:red">찰나적 관계</span>
- 점선 화살표, 단방향
- 연관 관계는 인스턴스들간에 <u>지속적으로 유지</u>될 때 사용

<h3>인터페이스와 실체화 관계</h3>

- 인터페이스란 <u>책임</u>이다.
- 어떤 공통되는 능력이 있는 것들을 대표하는 관점
- 실체화 관계는 점선, 속이 빈 삼각형으로 표현
- 실체화 관계의 또 다른 표현
  - provided interface
  - required interface
- keypoint
  - 일반화 관계는 is a kind of 관계이지만,
  - 실체화 관계는 can do this의 관계이다.

<br>

<h1>싱글턴패턴</h1>

- ```{readOnly, leaf}```
  - 읽을수만 있고 변경 불가 -> 상수 제약 조건 표현시 {}사용
- 싱글턴
  - 하나의 요소만을 갖는 집합
- lazy initialization
  - 인스턴스가 필요할 때 생성, 있다면 인스턴스 리턴
- <span style="color:red">race condition</span>
  - 쓰레드 경합
- ```synchronized```
  - 임계구역 설정, 특정 함수 동기화
  - CPU 주기적으로 체크 -> 성능에 부담
- <span style="color:red">DCL (Double Checked Locking)</span>
  - 2번 if문을 돌면서 체크
  - 일부만 함으로써 효율을 챙김
- <span style="color:red">Initialization on demand/lazy holder idiom</span>
  - 가장 많이 사용되는 싱글턴 구현 방식
  - volatile이나 synchronized 없이 동시성 문제 해결
- volatile
  - 코드 최적화를 위해 reorder를 금지하는 역할
  - DCL의 문제점을 해결할 수 있는 방안

<br>

<h1>객체지향 원리</h1>

<h3>추상화</h3>

- 모델링은 추상화에 바탕을 둠
  - 특정 관점에서 관련이 있는점은 부각, 관련이 없는 것은 무시
- 어떤 영역에서 필요로 하는 속성이나 행위를 추출
  - 관심 부분에 더욱 집중

<h3>캡슐화</h3>

- 관련있는 정보를 한 곳에 그룹핑
- 캡슐화를 통해 <span style="color:red">높은 응집도와 낮은 결합도를 갖는 설계</span>

<h3>클래스</h3>

- 캡슐화를 제공하는 수단
- 관련된 속성과 메소드를 가짐

<h3>정보 은닉 information hiding</h3>

- 정보를 은닉함으로써 결합도를 낮출 수 있다. -> 외부에서의 영향을 덜 받거나 받지 않게 됨.
- ex) private으로 속성 선언

<h3>일반화 관계 (≠상속 관계)</h3>

- 철학에서 일반화는 "여러 개체들이 가진 공통된 특성을 부각시켜 <span style="color:red">하나의 개념이나 법칙으로 성립시키는 과정</span>"
- 일반화는 클래스 자체를 캡슐화하여 <span style="color:red">변경에 대비할 수 있는 설계</span>를 가능케 한다.
  - 새로운 클래스가 추가되더라도 클라이언트는 영향 받지 않도록 -> 즉, SOLID 원칙 중 OCP를 위반하지 않도록

<h3>위임 Delegation</h3>

- 어떤 클래스의 <span style="color:red">일부 기능만을 사용하고 싶을 경우</span>에 사용

<h3>피터 코드의 상속 규칙</h3>

- 자식클래스와 부모 클래스 간 <u>'역할 수행' 관계가 아니어야 한다.</u>
- 한 클래스의 인스턴스는 <u>다른 서브 클래스의 객체로 변환할 필요가 절대 없어야 한다.</u>
- 자식 클래스가 부모 클래스의 책임을 무시하거나 재정의하지 않고 <u>확장만 수행해야 한다.</u>
- 자식 클래스가 단지 일부 기능을 <u>재사용할 목적으로 유틸리티 역할을 수행하는 클래스를 상속하지 않아야 한다,</u>
- 자식 클래스가 '역할', '트랜잭션', '디바이스' 등을 <u>특수화해야 한다.</u>

<br>

<h1>Builder 패턴</h1>

<h3>빌더 패턴</h3>

- <span style="color:red">객체 생성 패턴</span>
- 생성자의 <u>인자가 많은</u> 경우
- <u>필수적 인자와 선택적 인자가 혼합</u>되어 있는 경우
- <u>Immutable 객체(변경할 수 없는 객체)를 생성</u>하고 싶은 경우

<h3><span style="color:red">Telescoping Constructor 패턴</span> (점층적 생성자 패턴)</h3>

- 필수 인자를 받는 생성자를 정의한 후에 선택적 인자를 추가로 받는 생성자를 계속해서 정의
  - 필수 인자 생성자 -> 선택적 인자 생성자
- 문제점
  - 인자가 많을수록 생성자 개수도 많아진다.
  - 생성자의 인자가 어떤 의미인지 파악하기 힘들다.
  - 동일한 타입 인자인 경우 가독성이 떨어진다.

<h3><span style="color:red">JavaBeans 패턴</span></h3>

- Telescoping Constructor 패턴의 문제를 해결하고자 함
- <u>Setter 메소드로 각 속성의 값을 설정</u>
- 가독성은 향상되나 <u>Immutable object를 만들 수 없음</u>
  - 생성자를 통해 객체 생성 후 setter를 통해 값이 바뀔 수 있기 때문에..

<h3><span style="color:red">Builder 패턴</span></h3>

```java
public class Book {
  private Long id;
  ...
    
  public static class BookBuilder{
    ...
  }
}
```

- 장점
  - 가독성 개선
  - 메소드 체인닝
  - Immutable 객체 생성
- 단점
  - 코드 길이 증가

```java
Book book = new Book.BookBuilder(1L,"isbn1234")
  .author("insang")
  .pages(360).category("ce")
  .title("Design Pattern")
  .build();
```

<h3><span style="color:red">Lombok</span> @Builder 어노테이션 사용</h3>

- Getter/Setter/Builder 자동생성

  ```java
  @Getter
  @Builder
  public class LombokBook{
    @NonNull // 필수적 인자를 선언할 때
    private Long id;
  	...
    private String title;
  }
  ```

- Main에서 사용 시

  ```java
  LombokBook book = new LombokBook.LombokBookBuilder()
    .id(1L)
    .title("Design Pattern")
    ......
    .build();
  ```

<br>

<h1>SOLID</h1>

<h3>SOLID</h3>

- 로버트 마틴이 주창한 다섯 가지 설계 원칙
- Design Pattern의 기반이 됨.
  - <span style="color:red">SRP</span>
    - 단일 책임 원칙
    - Single Responsibility Principle
  - <span style="color:red">OCP</span>
    - 개방 폐쇄 원칙
    - Open Closed Principle
  - <span style="color:red">LSP</span>
    - 리스코프의 대입 원칙
    - Liskov Substitution Principle
  - <span style="color:red">ISP</span>
    - 인터페이스 분리 원칙
    - Interface Segregation Principle
  - <span style="color:red">DIP</span>
    - 의존성 역전 원칙
    - Dependency Inversion Principle
- good SW
  - 이해하기 쉽다.
  - 변경 및 유지 보수에 용이
  - 확장하기 쉽다.

<h3>SRP</h3>

- <span style="color:red">단일 책임 원칙</span>
- 클래스는 <u>단 하나의 책임만을 가지도록</u> 설계해야 한다.
- 책임
  - <u>Actor</u>
    - 동일한 needs나 기대를 가지는 사용자 <u>그룹</u>
  - 한 actor의 요구사항을 만족시키기 위한 기능들의 모임
- 한 클래스는 한(one and only one) actor만을 책임져야 한다.
  - 하나의 클래스 -> 하나의 Actor (사용자 그룹)
  - 클래스를 분리

<h3>OCP</h3>

- SOLID의 다섯 가지 원칙 중 가장 핵심이 되는 원칙
- <span style="color:red">개방 폐쇄의 원칙</span>
- <u>기존의 코드를 변경하지 않으면서 새로운 기능을 추가</u>할 수 있도록 설계
- OCP를 만족하는 설계가 되기 위해서는...
  - 변하는 것을 식별하고
  - 변하는 것을 <u>클래스로 분리</u>한다. (캡슐화)
  - 변하는 것들을 포용하는 개념을 추상 클래스나 인터페이스로 <u>추상화</u>한다.
  - 2번 단계에서 만든 클래스를 3번 단계에서 추출한 추상화된 개념의 자식 클래스로 모델링한다.

<h3>LSP</h3>

- <u>일반화 관계를 적절하게 사용했는지를 점검</u>하는 원칙
- LSP는 일반화 관계는 슈퍼 클래스가 제공하는 오퍼레이션과 파생클래스에서 제공하는 오퍼레이션 간에는 <span style="color:red">행위적으로 일관성이 있도록</span> 설계가 되어야 한다는 원칙
- 프로그램에서 <span style="color:red">슈퍼 클래스의 인스턴스 대신에 파생 클래스의 인스턴스로 대체하여도 프로그램의 의미는 변화되지 않도록</span> 설계
  - 슈퍼 클래스의 인스턴스보다 파생 클래스의 인스턴스가 일이 더 많아야 함 (확장의 개념)
- 행위 일관성
  - 상위 클래스
    - pre : 선조건
    - post : 후조건
  - 하위 클래스
    - pre' : 선조건
    - post' : 후조건
  - pre => pre'
    - 만약 선조건 pre가 만족된다면 pre'가 만족되어야 한다.
  - post' => post
    - 만약 후조건 post'가 만족된다면 post가 만족되어야 한다.
  - ex)
    - 상위 클래스 : 불이 난다면 (pre), 사람을 구한다. (post)
    - 하위 클래스 : 불이나 홍수가 난다면 (pre'), 생명을 구한다. (post')

<h3>ISP</h3>

- <span style="color:red">인터페이스 분리 원칙</span>
  - "Clients should not be forced to depend upon interfaces that they do not use."
  - <u>인터페이스를 클라이언트에 특화되도록 분리</u>해야하는 설계 원칙
    - fat interface -> small interface
  - 클라이언트의 관점에서 클라이언트 자신이 이용하지 않는 기능에는 영향을 받지 않아야 한다는 내용이 담겨 있다.

<h3>DIP</h3>

- <span style="color:red">의존성 역전 원칙</span>
- 상위 모듈은 하위 모듈에 의존하면 안된다. 이 두 모듈 모두 <u>다른 추상화된 것에 의존</u>해야 한다.
  - High-level modules should not depend on low-level modules. Both should depend on abstractions.
- 추상화된 것은 구체적인 것에 의존하면 안된다. <u>구체적인 것이 추상화된 것에 의존</u>해야 한다.
  - Abstractions should not depend on details (concrete implementation). Details should depend on abstraction
- <u>High-level module</u>
  - 도메인 핵심 로직 domain <u>core</u> logic
- <u>Low-level module</u>
  - 도메인 <u>핵심 로직을 둘러싼 환경</u>
  - 도메인 핵심 로직에 필요한 정보를 제공하거나 도메인 핵심 로직으로부터 생성된 정보를 외부에 전달
  - 변경될 가능성이 많다.
- 도메인 핵심 로직이 주변 환경의 변화에 영향 받지 않도록 설계
  - 의존 관계를 맺을 때 도메인 핵심 로직으로 의존 관계 방향이 설정 되어 있어야 한다.
- 의존 관계를 설정할 때에는 구체적인 클래스 보다는 이를 추상화한 개념과 <span style="color:red">인터페이스 같은 수단을 이용하여 관계를 맺도록</span> 설계해야 한다.

<br>

- 패키지 분리
  - 패키지
    - 관련 있는 것들을 묶는 수단
    - 외부와 상관없이 독립적으로 배포가 가능함

<br>

<h1>Strategy</h1>

<h3>스트래티지 패턴</h3>

- 전략을 쉽게 바꿀수 있도록 해주는 디자인 패턴
- <span style="color:red">전략</span>
  - 어떤 목적을 달성하기 위해 일을 수행하는 방식, 비즈니스 규칙, 문제를 해결하는 알고리즘

<br>

<h1>Command</h1>

<h3>커맨드 패턴</h3>

- <u>이벤트가 발생했을 때</u> 실행될 기능이 다양하면서 변경이 필요한 경우 <u>이벤트를 발생시키는 클래스의 변경없이 재사용하고자 할 때</u>
- 커맨트 패턴은 실행될 기능을 캡슐화함으로써 기능의 실행을 요구하는 호출자 클래스 (Invoker)와 실제 기능을 수행하는 수신자 클래스 (Receiver) 사이의 의존성을 제거한다. 따라서 실행될 기능의 변경에도 호출자 클래스를 수정없이 그대로 사용할 수 있도록 해준다.

<h3><span style="color:red">Starategy vs Command</span></h3>

- 공통적인 내용
  - 변하는 것을 식별하고
  - 변하는 것을 클래스로 분리한다. (캡슐화)
  - 변하는 것들을 포용하는 개념을 추상 클래스나 인터페이스로 추상화한다.
  - 2번 단계에서 만든 클래스를 3번 단계에서 추출한 추상화된 개념의 자식 클래스로 모델링한다.
- 차이점
  - Strategy
    - 한 클래스가 <u>동일한</u> 목적을 가지는 둘 이상의 기능을 수행할 때
  - Command
    - 한 클래스가 <u>동일하지 않은</u> 목적을 가지는 둘 이상의 기능을 수행할 때

