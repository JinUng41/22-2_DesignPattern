# Observer Pattern

>행위 behavioral 패턴

## 옵서버 패턴

- 데이터의 변경이 발생하였을 때,
- 상대 클래스 및 객체에 의존하지 않으면서
- 데이터 변경을 통보하고자 할 때

<br>

- 옵서버 패턴은 통보 대상 객체의 관리를 Subject 클래스와 Observer 인터페이스로 일반화한다.
- 그러면 데이터 변경을 통보하는 클래스 (ConcreteSubject)는 통보 대상 클래스/객체(ConcreteObserver)에 대한 의존성을 제거할 수 있다.
- 결과적으로 옵서버 패턴은 통보 대상 클래스나 대상 객체의 변경에도 ConcreteSubject 클래스를 수정 없이 그대로 사용할 수 있도록 한다.

<br>


- Subject
    - ConcreteObserver 객체를 관리하는 abstract 클래스
- Observer
    - interface, 다중성 : *
    - 데이터의 변경을 통보 받는 인터페이스
- ConcreteSubject
    - 변경 관리 대상이 되는 데이터가 있는 클래스
- ConcreteObserver
    - ConcreteSubject의 변경을 통보 받는 클래스


<br>

# Decorator Pattern

>구조 structural 패턴

## 데커레이터 패턴

- 기본 기능에 추가할 수 있는 기능의 종류가 많은 경우

<br>


- 데코레이터 패턴은 기본 기능에 추가될 수 있는 많은 수의 부가 기능에 대해서 다양한 조합을 동적으로 구현할 수 있는 패턴이다.

<br>


- 데커레이터 패턴은 새로운 부가 기능에 대해 OCP를 만족하는 설계이다.
- Component
    - 기본 기능을 뜻하는 ConcreteComponent와 추가 기능을 뜻하는 Decorator의 공통 기능을 정의
- ConcreteComponent
    - 기본 기능을 구현하는 클래스
- Decorator
    - 많은 수가 존재하는 구체적인 Decorator의 공통 기능을 정의
- ConcreteDecorator A,B,,,,
    - 기본 기능에 추가되는 개별적인 기능을 정의


<br>


# Template Method Pattern

>행위 behavioral 패턴

## 템플릿 메서드 패턴

- 전체적으로 동일하면서 부분적으로 상이한 문장을 가지는 메소드의 코드 중복을 최소화할 때 유용

<br>


- 템플릿 메소드 패턴은 전체적인 알고리즘을 구현하면서 상이한 부분은 하위 클래스에서 구현할 수 있도록 해 주는 디자인 패턴으로서 전체적인 알고리즘의 코드를 재사용하는 데 유용하다.

<br>


- AbstractClass
    - 템플릿 메서드를 정의하는 클래스
    - 하위 클래스에 공통 알고리즘을 정의하고,
    - 하위 클래스에서 구현될 기능을 primitive Operation으로 정의
- ConcreteClass
    - 상위 클래스에 구현된 템플릿 메서드의 일반적인 알고리즘에서
    - 하위 클래스에 적합하게 primitive Operation을 오버라이드하는 클래스
- primitive 메서드 = Hook 메서드

<br>

# Factory Method Pattern

>생성 creational 패턴

- 종류가 변경되거나 추가될 때,
- 변경이 자주 일어나는 부분을 클래스로 캡슐화한다.


<br>

- Factory Method로 캡슐화를 했을 때,
- 새로운 종류가 추가되어도 Factory Method만 수정하면 된다.

<br>

## GoF의 Factory Method 패턴

- Gang of Four
- Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides
- 객체를 생성하기 위해 인터페이스를 정의하지만,
- 어떤 클래스의 인스턴스를 생성할지에 대한 결정은 하위클래스가 담당

- Product
    - 팩토리 메서드로 생성될 객체의 공통 인터페이스
- ConcreteProduct
    - 구체적으로 객체가 생성되는 클래스
- Creator
    - 팩토리 메서드를 갖는 클래스
- ConcreteCreator
    - 팩토리 메서드를 구현하는 클래스로서 ConcreteProduct 객체를 생성

<br>

### Template method 활용
- 상위 클래스에서는 일반적인 흐름을 정의하고,
- 하위 클래스에서는 특정 부분을 재정의한다.

<br>

# Abstract Factory Pattern

>생성 creational 패턴

## 추상 팩토리 패턴

- 관련성이 있는 여러 종류의 객체를 일관된 방식으로 생성하는 경우에 유용
- 추상 팩토리 패턴은 관련성이 있는 여러 종류의 객체들을 일관된 방식으로 생성할 때 유용하다.


<br>

- AbstractFactory
    - 실제 팩토리 클래스의 공통 인터페이스
- ConcreteFactory
    - 구체적인 팩토리 클래스로 AbstractFactory의 추상 메서드를 오버라이드 함으로써 구체적인 제품을 생성
- AbstractProduct
    - 제품의 공통 인터페이스
- ConcreteProduct
    - 구체적인 팩토리 클래스에서 생성되는 구체적인  제품