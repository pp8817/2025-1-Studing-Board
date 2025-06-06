**추상 클래스 (Abstract Class)**

- 구현내용이 없는 메소드
- 추상 메소드가 하나라도 있는 클래스
- 추상 클래스는 그 자체로 객체를 생성
- 추상 클래스를 상속받은 클래스는 해당 메소드를 필수적으로 구현
- 상속을 통해서만 객체를 생성해서 사용할 수 있음

---

**인터페이스 (Interface)**

- 속성은 포함되지 않고, 추상 메소드와 같은 메소드 정의만 존재 하는 클래스
- 모양은 클래스와 유사하나 전혀 다른 개념
- 메소드는 구현할 수 없으며, 인터페이스를 구현(상속)하는 클래스에서 메소드를 반드시 구현해야 함
- implements 키워드를 사용하여 구현(상속)
- 다중 구현 가능
- 인터페이스로 객체를 만들 수 X. 자식 클래스만 객체 생성 가능
- 여러 클래스가 **공통된 동작을 강제**하도록!!!

---

## 기본 자료형 (Primitive Types)이란?

- 가장 기본적인 데이터 저장 방식
- 클래스가 아닌, **값 자체를 저장하는 변수**

| 자료형 | 설명 | 예시 |
| --- | --- | --- |
| int | 정수 | int a = 10; |
| double | 실수 | double pi = 3.14; |
| char | 문자 하나 | char c = 'A'; |
| boolean | 논리형 | boolean flag = true; |

### 🔸 장점

- **메모리 적게 사용**
- **빠름** (객체 생성이 없기 때문에)

### 🔸 단점

- **객체가 아님** → 객체로서의 기능(메서드, 제네릭 사용 등)을 사용하지 못함
- 예: int는 .compareTo() 같은 메서드가 없음

## 래퍼 클래스 (Wrapper Class)란?

- Wrapper Class는 기본 자료형을 **객체(Object)로 포장한 클래스**

| 기본형 | 래퍼 클래스 |
| --- | --- |
| byte | Byte |
| short | Short |
| int | Integer |
| long | Long |
| float | Float |
| double | Double |
| char | Character |
| boolean | Boolean |
| void | Void |

### 🔸 목적

- 기본 자료형을 객체로 다루기 위해 사용
1. **컬렉션 클래스 사용 시**
    - ArrayList<int> ❌ 불가능
    - ArrayList<Integer> ✅ 가능
        
        (제네릭은 객체 타입만 받음)
        
2. **객체로서 메서드를 사용하고 싶을 때**
    
    
java
    Integer x = 10;
    Integer y = 20;
    System.out.println(x.compareTo(y)); // -1 (비교 기능)

    
3. **null을 표현하고 싶을 때**
    - 기본 자료형은 null을 가질 수 없음
    - 래퍼 클래스는 null 가능 → DB와 연동 시 중요!

## 자동 박싱 / 언박싱 (Auto Boxing / Unboxing)

- Java 5부터는 **기본 자료형**과 **래퍼 클래스 간 변환**을 **자동**으로 **처리**해줌

### 🔹 박싱 (Boxing) : 기본형 → 객체

java
int a = 5;
Integer boxed = a;  // 자동 박싱


### 🔹 언박싱 (Unboxing) : 객체 → 기본형

java
Integer obj = 10;
int b = obj;  // 자동 언박싱


### 🔹 캐싱(Caching)

- 자주 사용하는 데이터를 미리 저장해두고, 다시 사용할 때 새로 만들지 않고 저장된 걸 **재사용**하는 것

---

## **Set : 집합**

- 중복된 내용은 저장 되지 않는다.
- 순서가 없다.
- index 가 없다.
- 수학의 집합과 같은 특성을 가진 자료구조를 **Set** 이라고 한다.

## **Set의 종류**

## **HashSet**

- 일반적으로는 HashSet을 사용한다.
- 집합 연산과 같다.

## **TreeSet**

- 값을 정렬한다.
- HashSet보다 상대적으로 느리다.

---

## Map

- **key**와 **value** 쌍으로 이루어진다.
- **key**를 통해서 **value** 를 찾는다.
- **key**는 중복 될 수 없고, **value**는 중복 가능하다.
- **key**를 통해서값을 찾는 속도가 빠르다.
- **value**를 통해서 key 찾는 작업은 느리다.
- 해당 자료형을 **Map** 이라고 한다.
