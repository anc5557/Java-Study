# Java-Study
작성자 : 서준호
일자 : 2023-12-18 ~ 2023-12-19

# 1. 변수와 데이터 타입

## 변수란?

- 변수는 데이터를 저장하기 위한 메모리 공간입니다.
- 변수에는 데이터 타입에 따라 다른 종류의 데이터를 저장할 수 있습니다.
- 변수는 특정 이름을 가지며, 이 이름을 사용하여 저장된 데이터에 접근할 수 있습니다.

## 자바의 기본 데이터 타입

- 자바에는 여러 가지 데이터 타입이 있으며, 크게 두 가지로 나뉩니다: **기본형**과 **참조형**
	1. **기본형(Primitive Types)**:
	    - **정수형**: `byte`, `short`, `int`, `long`
	    - **실수형**: `float`, `double`
	    - **문자형**: `char`
	    - **논리형**: `boolean`
	2. **참조형(Reference Types)**
	    - 객체의 주소를 저장하는 타입입니다.
	    - 예: `String`, 배열, 클래스 등

## 변수 선언과 초기화

```java

public class HelloWorld { 
	public static void main(String[] args) { 
		
		int number; // 'number'라는 이름의 int 타입 변수 선언
		number = 10; // 선언된 변수에 10을 할당
		
		String text; // 'text'라는 이름의 String 타입 변수 선언
		text = "Hello, Java!"; // 선언된 변수에 문자열 할당

		// 선언과 동시에 초기화 
		int anotherNumber = 20;
		String anotherText = "Welcome to Java World!"; 
		
		System.out.println(number);
		System.out.println(text);
		System.out.println(anotherNumber);
		System.out.println(anotherText);

	} 
}
```

# 2. 연산자

## (1) **산술 연산자 (Arithmetic Operators)**: 
   - `+` (더하기)
   - `-` (빼기)
   - `*` (곱하기)
   - `/` (나누기)
   - `%` (나머지)
## (2) **비교 연산자 (Comparison Operators)**: 
   - `==` (같음)
   - `!=` (다름)
   - `>` (크다)
   - `<` (작다)
   - `>=` (크거나 같다)
   - `<=` (작거나 같다)
## (3) **논리 연산자 (Logical Operators)**: 
   - `&&` (논리곱, AND)
   - `||` (논리합, OR)
   - `!` (논리 부정, NOT)
## (4) **할당 연산자 (Assignment Operators)**: 
   - `=` (할당)
   - `+=` (더한 값 할당)
   - `-=` (뺀 값 할당)
   - `*=` (곱한 값 할당)
   - `/=` (나눈 값 할당)
   - `%=` (나머지 할당)
## (5) **증감 연산자 (Increment/Decrement Operators)**: 
   - `++` (증가)
   - `--` (감소)
   
## 예제: 연산자

```java
public class OperatorExample {
    public static void main(String[] args) {
        int a = 10;
        int b = 5;

        // 산술 연산자 사용
        System.out.println("a + b = " + (a + b));
        System.out.println("a - b = " + (a - b));
        System.out.println("a * b = " + (a * b));
        System.out.println("a / b = " + (a / b));
        System.out.println("a % b = " + (a % b));

        // 비교 연산자 사용
        System.out.println("a == b: " + (a == b));
        System.out.println("a != b: " + (a != b));
        System.out.println("a > b: " + (a > b));
        System.out.println("a < b: " + (a < b));
        System.out.println("a >= b: " + (a >= b));
        System.out.println("a <= b: " + (a <= b));

        // 논리 연산자 사용
        boolean x = true;
        boolean y = false;
        System.out.println("x && y: " + (x && y));
        System.out.println("x || y: " + (x || y));
        System.out.println("!x: " + (!x));

        // 할당 연산자 사용
        int c = 10;
        c += 5; // c = c + 5와 동일
        System.out.println("c: " + c);

        // 증감 연산자 사용
        int d = 10;
        d++;
        System.out.println("d: " + d);
        d--;
        System.out.println("d: " + d);
    }
}
```

# 3. 조건문

`if`, `else`, `else if`, `switch` 문을 사용

## (1) `if` 문
`if` 문은 주어진 조건이 참(True)일 때 코드 블록을 실행합니다.

```java
if (조건) {
    // 조건이 참일 때 실행할 코드
}
```

## (2) `else` 문
`else` 문은 `if` 문의 조건이 거짓(False)일 때 실행되는 코드 블록입니다.

```java
if (조건) {
    // 조건이 참일 때 실행할 코드
} else {
    // 조건이 거짓일 때 실행할 코드
}
```

## (3) `else if` 문
`else if` 문은 여러 조건 중 하나를 선택하여 실행할 때 사용합니다. `if` 문 다음에 여러 개의 `else if` 문을 사용할 수 있습니다.

```java
if (조건1) {
    // 조건1이 참일 때 실행할 코드
} else if (조건2) {
    // 조건1이 거짓이고 조건2가 참일 때 실행할 코드
} else {
    // 모든 조건이 거짓일 때 실행할 코드
}
```

## (4) `switch` 문
`switch` 문은 하나의 변수나 표현식을 여러 값과 비교할 때 유용합니다.

```java
switch (변수) {
    case 값1:
        // 변수가 값1과 일치할 때 실행할 코드
        break;
    case 값2:
        // 변수가 값2와 일치할 때 실행할 코드
        break;
    // 추가 케이스들...
    default:
        // 어떤 케이스에도 해당되지 않을 때 실행할 코드
}
```

## 예제: 조건문

```java
public class ConditionalStatements {
    public static void main(String[] args) {
        int number = 25;

        // if, else if, else 사용
        if (number > 30) {
            System.out.println("number는 30보다 큽니다.");
        } else if (number > 20) {
            System.out.println("number는 20보다 크고 30보다 작거나 같습니다.");
        } else {
            System.out.println("number는 20 이하입니다.");
        }

        // switch 사용
        int day = 4;
        switch (day) {
            case 1:
                System.out.println("월요일");
                break;
            case 2:
                System.out.println("화요일");
                break;
            case 3:
                System.out.println("수요일");
                break;
            case 4:
                System.out.println("목요일");
                break;
            case 5:
                System.out.println("금요일");
                break;
            case 6:
                System.out.println("토요일");
                break;
            case 7:
                System.out.println("일요일");
                break;
            default:
                System.out.println("유효하지 않은 요일");
        }
    }
}
```


# 4. 반복문

## (1) `for` 반복문
`for` 반복문은 특정 횟수만큼 반복하고자 할 때 주로 사용됩니다. 초기화, 조건 검사, 그리고 반복 후 작업(증가/감소)을 한 곳에 정의할 수 있습니다.

```java
for (초기화; 조건; 증가/감소) {
    // 반복할 코드
}
```

## (2) `while` 반복문
`while` 반복문은 주어진 조건이 참인 동안 계속해서 코드 블록을 반복 실행합니다.

```java
while (조건) {
    // 반복할 코드
}
```

## (3) `do-while` 반복문
`do-while` 반복문은 블록 내의 코드를 최소 한 번 실행한 후 조건을 검사합니다. 이것은 조건에 상관없이 최소 한 번은 코드를 실행하고 싶을 때 유용합니다.

```java
do {
    // 반복할 코드
} while (조건);
```

## 예제: 반복문
```java
public class LoopExample {
    public static void main(String[] args) {
        // for 반복문 예제
        System.out.println("for 반복문:");
        for (int i = 1; i <= 5; i++) {
            System.out.println("i = " + i);
        }

        // while 반복문 예제
        System.out.println("\nwhile 반복문:");
        int j = 1;
        while (j <= 5) {
            System.out.println("j = " + j);
            j++;
        }

        // do-while 반복문 예제
        System.out.println("\ndo-while 반복문:");
        int k = 1;
        do {
            System.out.println("k = " + k);
            k++;
        } while (k < 1);
    }
}
```



# 배열
## (1) 배열의 선언과 초기화

1. **선언과 동시에 초기화**
   ```java
   int[] myArray = {1, 2, 3, 4, 5};
   ```

2. **빈 배열 선언 후 나중에 초기화**
   ```java
   int[] myArray;
   myArray = new int[5]; // 5개의 요소를 가진 배열
   ```

3. **선언과 함께 특정 크기로 초기화**
   ```java
   int[] myArray = new int[5]; // 5개의 요소를 가진 배열
   ```

## (2) 배열 요소에 접근하기

배열의 각 요소에는 인덱스를 통해 접근할 수 있습니다. 인덱스는 0부터 시작합니다.

```java
myArray[0] = 10; // 첫 번째 요소에 값 할당
int value = myArray[0]; // 첫 번째 요소의 값 읽기
```

## (3) 배열과 반복문
배열의 모든 요소를 순회하거나 처리할 때는 반복문이 유용합니다.

```java
for (int i = 0; i < myArray.length; i++) {
    System.out.println(myArray[i]);
}
```

## 예제: 배열 
```java
public class ArrayExample {
    public static void main(String[] args) {
        // 배열 선언 및 초기화
        int[] numbers = {1, 2, 3, 4, 5};

        // 배열의 길이 출력
        System.out.println("배열의 길이: " + numbers.length);

        // 배열의 모든 요소 출력
        System.out.println("배열의 요소:");
        for (int i = 0; i < numbers.length; i++) {
            System.out.println(numbers[i]);
        }

        // 배열 요소의 합 계산
        int sum = 0;
        for (int number : numbers) {
            sum += number;
        }
        System.out.println("요소의 합: " + sum);
    }
}
```

# 컬렉션 프레임워크

자바의 컬렉션 프레임워크는 데이터를 효율적으로 처리하고 저장하기 위한 다양한 클래스와 인터페이스를 제공합니다. 컬렉션은 크게 `List`, `Set`, `Map` 세 가지 주요 인터페이스로 구분됩니다.

## (1) `List` 인터페이스
- **순서가 있는 컬렉션**을 나타냅니다.
- 같은 요소의 중복 저장이 가능합니다.
- 대표적인 구현 클래스로는 `ArrayList`, `LinkedList` 등이 있습니다.

### 예시: `ArrayList`
```java
import java.util.ArrayList;
import java.util.List;

public class ListExample {
    public static void main(String[] args) {
        List<String> fruits = new ArrayList<>();
        fruits.add("사과");
        fruits.add("바나나");
        fruits.add("오렌지");
        fruits.add("사과"); // 중복 요소 추가

        for (String fruit : fruits) {
            System.out.println(fruit);
        }
    }
}
```

###  예시: `LinkedList`
`LinkedList`는 리스트 인터페이스를 구현한 연결 리스트입니다. 데이터의 삽입과 삭제가 빈번할 때 유용합니다.

```java
import java.util.LinkedList;
import java.util.List;

public class LinkedListExample {
    public static void main(String[] args) {
        LinkedList<String> animals = new LinkedList<>();
        animals.add("사자");
        animals.add("호랑이");
        animals.add("기린");

        animals.addFirst("코끼리"); // 리스트 맨 앞에 추가
        animals.addLast("판다"); // 리스트 맨 뒤에 추가

        for (String animal : animals) {
            System.out.println(animal);
        }
    }
}
```


## (2) `Set` 인터페이스
- **중복을 허용하지 않는 컬렉션**을 나타냅니다.
- 순서를 보장하지 않습니다.
- 대표적인 구현 클래스로는 `HashSet`, `LinkedHashSet`, `TreeSet` 등이 있습니다.

### 예시: `HashSet`
```java
import java.util.HashSet;
import java.util.Set;

public class SetExample {
    public static void main(String[] args) {
        Set<String> cities = new HashSet<>();
        cities.add("서울");
        cities.add("부산");
        cities.add("대구");
        cities.add("서울"); // 중복된 요소, 저장되지 않음

        for (String city : cities) {
            System.out.println(city);
        }
    }
}
```


### 예시:  `LinkedHashSet`
`LinkedHashSet`은 `HashSet`의 순서가 보장되는 버전입니다. 삽입 순서를 유지합니다.

```java
import java.util.LinkedHashSet;
import java.util.Set;

public class LinkedHashSetExample {
    public static void main(String[] args) {
        Set<Integer> numbers = new LinkedHashSet<>();
        numbers.add(2);
        numbers.add(3);
        numbers.add(1);

        for (Integer number : numbers) {
            System.out.println(number); // 삽입 순서대로 출력됨
        }
    }
}
```

### 예시: `TreeSet`
`TreeSet`은 정렬된 순서로 요소를 저장하는 세트 컬렉션입니다. 자동으로 정렬됩니다.

```java
import java.util.TreeSet;
import java.util.Set;

public class TreeSetExample {
    public static void main(String[] args) {
        Set<String> fruits = new TreeSet<>();
        fruits.add("바나나");
        fruits.add("사과");
        fruits.add("키위");

        for (String fruit : fruits) {
            System.out.println(fruit); // 정렬된 순서로 출력됨
        }
    }
}
```

## (3) `Map` 인터페이스
- **키(Key)와 값(Value)의 쌍**으로 데이터를 저장합니다.
- 키는 중복될 수 없으며, 각 키는 하나의 값을 가집니다.
- 대표적인 구현 클래스로는 `HashMap`, `TreeMap`, `LinkedHashMap` 등이 있습니다.

### 예시: `HashMap`
```java
import java.util.HashMap;
import java.util.Map;

public class MapExample {
    public static void main(String[] args) {
        Map<String, Integer> ageOfFriends = new HashMap<>();
        ageOfFriends.put("철수", 20);
        ageOfFriends.put("영희", 25);
        ageOfFriends.put("민수", 30);

        for (Map.Entry<String, Integer> entry : ageOfFriends.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```


### 예시: `TreeMap`
`TreeMap`은 키를 기준으로 정렬된 맵 컬렉션입니다. 키에 의한 자동 정렬 기능을 제공합니다.

```java
import java.util.TreeMap;
import java.util.Map;

public class TreeMapExample {
    public static void main(String[] args) {
        Map<String, Integer> scores = new TreeMap<>();
        scores.put("철수", 85);
        scores.put("영희", 92);
        scores.put("민수", 75);

        for (Map.Entry<String, Integer> entry : scores.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

### 예시: `LinkedHashMap`
`LinkedHashMap`은 `HashMap`과 비슷하지만, 삽입된 순서 혹은 접근된 순서를 유지합니다.

```java
import java.util.LinkedHashMap;
import java.util.Map;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        Map<String, String> capitals = new LinkedHashMap<>();
        capitals.put("한국", "서울");
        capitals.put("일본", "도쿄");
        capitals.put("중국", "베이징");

        for (Map.Entry<String, String> entry : capitals.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

`List`는 순서가 중요하거나 중복된 요소를 허용해야 할 때, 
`Set`은 중복을 허용하지 않고 순서가 중요하지 않을 때, 
`Map`은 키-값 쌍으로 데이터를 저장해야 할 때 적합합니다. 

# 메소드

메소드(Method)는 자바 프로그래밍의 핵심 요소 중 하나로, 특정 작업을 수행하는 코드의 묶음입니다. 메소드를 사용하면 코드를 재사용하고, 관리하기 쉽고, 가독성이 좋은 프로그램을 만들 수 있습니다.

## (1) 메소드의 기본 구성요소

1. **메소드 선언**: 메소드를 정의하는 부분으로, 메소드의 이름, 반환 타입, 매개변수 목록, 접근 제어자 등을 포함합니다.
2. **메소드 몸체**: 메소드의 실제 작업을 수행하는 코드 블록입니다.

## (2) 메소드 선언 방법

메소드 선언의 일반적인 형태는 다음과 같습니다:

```java
접근제어자 반환타입 메소드이름(매개변수목록) {
    // 메소드 몸체
    // 작업 수행 코드
}
```

- **접근 제어자(Access Modifier)**: 메소드가 어디서 접근 가능한지를 결정합니다. (`public`, `private`, `protected` 등)
- **반환 타입(Return Type)**: 메소드가 실행된 후 반환하는 값의 데이터 타입입니다. 반환 값이 없을 경우 `void`로 지정합니다.
- **메소드 이름(Method Name)**: 메소드를 호출할 때 사용하는 이름입니다.
- **매개변수 목록(Parameter List)**: 메소드에 전달되는 입력 값으로, 없을 수도 있습니다.

## 예제: 메소드

1. **간단한 메소드 예시**: 두 수를 더하는 메소드
```java
public class SimpleMethod {
   public static void main(String[] args) {
	   int sum = add(10, 20);
	   System.out.println("합계: " + sum);
   }

   public static int add(int num1, int num2) {
	   return num1 + num2;
   }
}
```
   여기서 `add` 메소드는 두 정수를 입력받아 그 합을 반환합니다.

2. **매개변수가 없는 메소드**: 인사말을 출력하는 메소드
```java
public class NoParameterMethod {
   public static void main(String[] args) {
	   printGreeting();
   }

   public static void printGreeting() {
	   System.out.println("안녕하세요!");
   }
}
```
   `printGreeting` 메소드는 매개변수가 없으며, 호출될 때 "안녕하세요!"를 출력합니다.

3. **반환 값이 없는 메소드**: 두 수의 합을 출력하는 메소드
```java
public class NoReturnMethod {
   public static void main(String[] args) {
	   printSum(15, 25);
   }

   public static void printSum(int num1, int num2) {
	   int sum = num1 + num2;
	   System.out.println("합계: " + sum);
   }
}
```
   `printSum` 메소드는 두 수를 입력받아 그 합을 출력하지만, 값을 반환하지는 않습니다 (`void`).

# 클래스와 객체

## (1) 클래스(Class)

클래스는 객체를 만들기 위한 템플릿 또는 설계도와 같습니다. 객체의 상태를 나타내는 필드(변수)와 객체의 행동을 나타내는 메소드(함수)로 구성됩니다.

### 클래스 정의 방법

```java
public class ClassName {
    // 필드
    int field1;
    String field2;

    // 메소드
    void method1() {
        // 메소드 내용
    }

    int method2() {
        // 메소드 내용
        return 값;
    }
}
```

## (2) 객체(Object)
객체는 클래스에 정의된 내용을 바탕으로 생성된 실체입니다. 클래스의 인스턴스라고도 합니다. 실제 프로그램에서 클래스의 정의에 따라 메모리에 할당된 것이 객체입니다.

### 객체 생성 및 사용 방법

```java
public class Main {
    public static void main(String[] args) {
        // 객체 생성
        ClassName obj = new ClassName();

        // 필드 값 설정
        obj.field1 = 10;
        obj.field2 = "Hello";

        // 메소드 호출
        obj.method1();
        int result = obj.method2();
    }
}
```

### 예제: 클래스와 객체

```java
// Car 클래스 사용을 위한 Main 클래스
public class Main {
    public static void main(String[] args) {
        // Car 객체 생성
        Car myCar = new Car();

        // 필드 값 설정
        myCar.color = "Red";
        myCar.speed = 0;

        // 메소드 호출
        myCar.accelerate(); // 속도 증가
        System.out.println("현재 속도: " + myCar.speed);

        myCar.brake(); // 속도 감소
        System.out.println("현재 속도: " + myCar.speed);
    }
}

// Car 클래스 정의
class Car {
    // 필드(상태)
    String color;
    int speed;

    // 메소드(행동)
    void accelerate() {
        speed += 10; // 속도 증가
    }

    void brake() {
        speed -= 10; // 속도 감소
    }
}

```

## (3) 생성자

자바에서 생성자(Constructor)는 클래스의 인스턴스, 즉 객체가 생성될 때 자동으로 호출되는 특별한 메소드입니다. 생성자는 객체의 초기화를 담당하며, 필드(클래스 변수)의 초기 값을 설정하는 데 주로 사용됩니다.

### 생성자의 특징
1. **생성자의 이름은 클래스의 이름과 동일**해야 합니다.
2. 생성자는 **반환 타입을 가지지 않습니다** (void도 사용하지 않음).
3. 생성자는 **오버로딩(Overloading)이 가능**합니다. 즉, 같은 이름의 생성자를 매개변수의 타입이나 개수를 달리하여 여러 개 정의할 수 있습니다.

### 기본 생성자(Default Constructor)
- 클래스에 생성자가 명시적으로 정의되지 않으면, 자바 컴파일러는 기본 생성자를 자동으로 제공합니다.
- 기본 생성자는 매개변수가 없으며, 클래스의 필드를 기본값으로 초기화합니다.

### 사용자 정의 생성자
- 클래스에 맞춰 직접 생성자를 정의할 수 있습니다.
- 필드를 초기화하거나 객체 생성 시 필요한 설정을 수행할 수 있습니다.

### 예제: Car 클래스에 생성자 추가

```java

public class Main {
    public static void main(String[] args) {
        // Car 객체 생성 시 생성자 호출
        Car myCar = new Car("Red", 0);

        // 메소드 호출
        myCar.accelerate();
        System.out.println("현재 속도: " + myCar.speed);

        myCar.brake();
        System.out.println("현재 속도: " + myCar.speed);
    }
}

public class Car {
    String color;
    int speed;

    // 생성자
    public Car(String color, int speed) {
        this.color = color;
        this.speed = speed;
    }

    // 메소드
    void accelerate() {
        speed += 10;
    }

    void brake() {
        speed -= 10;
    }
}


```

이 예제에서 `Car` 클래스에는 색상과 속도를 초기화하는 사용자 정의 생성자가 추가되었습니다. `Main` 클래스에서 `Car` 객체를 생성할 때 이 생성자를 호출하여 초기 색상과 속도를 설정합니다.

생성자를 사용하면 객체 생성 시 필요한 초기화 작업을 간편하고 명확하게 수행할 수 있어, 객체의 사용을 보다 안전하고 효율적으로 만듭니다.


# 상속

상속은 한 클래스(자식 클래스)가 다른 클래스(부모 클래스)의 속성과 메소드를 물려받는 것을 의미합니다. 상속을 사용하면 코드 재사용성을 높이고, 유지보수를 용이하게 할 수 있습니다.

## (1) 기본 구조
```java
class 부모클래스 {
    // 부모 클래스의 필드와 메소드
}

class 자식클래스 extends 부모클래스 {
    // 자식 클래스의 추가적인 필드와 메소드
}
```

## (2) 특징
1. **재사용성**: 부모 클래스의 코드를 재사용하여 새로운 클래스를 만들 수 있습니다.
2. **확장성**: 기존 코드를 변경하지 않고, 새로운 기능을 추가하거나 기존 기능을 수정할 수 있습니다.

## (3) 상속의 주의점
- Java는 단일 상속만을 지원합니다. 즉, 하나의 클래스는 오직 하나의 클래스만 상속받을 수 있습니다.
- 최상위 클래스인 `Object` 클래스는 모든 클래스의 부모 클래스입니다.
- 상속받은 메소드를 자식 클래스에서 재정의(오버라이딩)할 수 있습니다. 이 때 `@Override` 어노테이션을 사용하는 것이 좋습니다.

## 예제: 상속 

```java
public class Main {
    public static void main(String[] args) {
        Car car = new Car();
        car.start();
        car.openDoor();
        car.stop();

        Bicycle bicycle = new Bicycle();
        bicycle.start();
        bicycle.ringBell();
        bicycle.stop();
    }
}

// 부모 클래스
class Vehicle {
    String type;

    void start() {
        System.out.println(type + "가 출발합니다.");
    }

    void stop() {
        System.out.println(type + "가 정지합니다.");
    }
}

// 자식 클래스
class Car extends Vehicle {
    Car() {
        this.type = "자동차";
    }

    void openDoor() {
        System.out.println("문을 엽니다.");
    }
}

class Bicycle extends Vehicle {
    Bicycle() {
        this.type = "자전거";
    }

    void ringBell() {
        System.out.println("종을 울립니다.");
    }
}
```

이 예제에서 `Vehicle` 클래스는 `type`, `start()`, `stop()`을 가지고 있으며, `Car`와 `Bicycle` 클래스는 `Vehicle`에서 상속받아 `type`을 설정하고 추가적인 기능인 `openDoor()`와 `ringBell()`을 구현합니다.

# 캡슐화

캡슐화는 객체 지향 프로그래밍의 중요한 원칙 중 하나로, 객체의 데이터(필드)와 그 데이터를 조작하는 메소드를 함께 묶어서, 데이터를 외부로부터 보호하고, 객체의 세부 구현을 숨기는 것을 말합니다.

## (1) 캡슐화의 핵심 개념
1. **데이터 은닉(Data Hiding)**: 클래스의 멤버 변수를 외부에서 직접 접근하지 못하도록 제한합니다. 이는 주로 필드를 `private` 접근 제어자로 선언함으로써 달성됩니다.
2. **퍼블릭 인터페이스 제공(Providing Public Interface)**: 외부에서 객체의 데이터에 접근하거나 수정할 수 있는 메소드를 제공합니다. 이들 메소드는 주로 `public`으로 선언되며, `getter`와 `setter`라고 불리는 메소드를 통해 필드의 값을 안전하게 읽고 변경할 수 있습니다.

## (2) 캡슐화의 장점
1. **보안**: 객체의 내부 데이터를 보호하여, 객체 외부에서는 잘못된 사용으로 인한 오류를 줄일 수 있습니다.
2. **유지보수 용이성**: 내부 구현을 외부로부터 분리함으로써, 내부 구현 변경 시 외부에 영향을 주지 않고 유지보수가 가능합니다.
3. **제어의 중앙화**: 데이터의 변경을 통제하고 검증할 수 있는 중앙 위치를 제공합니다.

## 예제: 캡슐화

```java
public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("홍길동");
        person.setAge(30);

        System.out.println("이름: " + person.getName());
        System.out.println("나이: " + person.getAge());
    }
}

class Person {
    // private 접근 제어자를 사용하여 데이터를 은닉
    private String name;
    private int age;

    // name 필드에 대한 getter 메소드
    public String getName() {
        return name;
    }

    // name 필드에 대한 setter 메소드
    public void setName(String name) {
        this.name = name;
    }

    // age 필드에 대한 getter 메소드
    public int getAge() {
        return age;
    }

    // age 필드에 대한 setter 메소드
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        }
    }
}
```

이 예제에서 `Person` 클래스는 `name`과 `age`라는 두 개의 `private` 필드를 가지고 있으며, 이 필드들에 접근하기 위한 `public` 메소드(`getName`, `setName`, `getAge`, `setAge`)를 제공합니다. 이렇게 함으로써 필드에 대한 접근을 제어하고, 필요한 경우 추가적인 검증 로직을 삽입할 수 있습니다. 

캡슐화를 통해 클래스의 내부 구현을 외부로부터 독립시키고, 데이터의 안전한 접근을 보장함으로써, 프로그램의 전체적인 안정성과 유지보수성을 높일 수 있습니다.

# 다형성
## (1) 다형성이란?
다형성은 '많은 형태를 가진다'는 의미로, 객체 지향 프로그래밍에서 하나의 객체가 여러 타입의 인스턴스로 취급될 수 있는 특성을 말합니다. 즉, 부모 클래스 타입의 참조 변수로 자식 클래스의 인스턴스를 참조할 수 있습니다.

## (2) 다형성의 장점
- **확장성**: 새로운 클래스를 추가하더라도 기존 코드를 변경하지 않고 확장할 수 있습니다.
- **유연성**: 프로그램 코드를 더 유연하게 작성할 수 있습니다.
- **유지보수성**: 코드를 간결하게 유지하며, 유지보수가 용이합니다.

## (3) 다형성의 주의점
- **타입 캐스팅**: 다형성을 사용할 때, 실제 인스턴스의 타입에 맞게 명시적으로 타입 캐스팅을 해야 하는 경우가 있습니다.
- **메소드 오버라이딩**: 다형성을 활용할 때, 메소드 오버라이딩이 중요한 역할을 합니다. 부모 클래스 타입으로 자식 클래스의 인스턴스를 다룰 때, 오버라이딩된 메소드가 호출됩니다.

## 예제: 다형성 

```java
public class Main {
    public static void main(String[] args) {
        // 다형성 사용
        Vehicle vehicle = new Car();
        vehicle.drive(); // Car의 drive 메소드 호출

        vehicle = new Bicycle();
        vehicle.drive(); // Bicycle의 drive 메소드 호출
    }
}

class Vehicle {
    void drive() {
        System.out.println("차량이 움직입니다.");
    }
}

class Car extends Vehicle {
    @Override
    void drive() {
        System.out.println("자동차가 달립니다.");
    }
}

class Bicycle extends Vehicle {
    @Override
    void drive() {
        System.out.println("자전거가 달립니다.");
    }
}
```

이 예제에서 `Vehicle` 클래스는 `drive` 메소드를 가지고 있고, `Car`와 `Bicycle` 클래스는 이를 상속받아 `drive` 메소드를 오버라이드(재정의)합니다. `Main` 클래스에서 `Vehicle` 타입의 참조 변수 `vehicle`을 사용하여 `Car`와 `Bicycle` 객체를 다룹니다. 이처럼 다형성을 사용하면, 하나의 참조 변수로 다양한 객체를 다룰 수 있습니다.

다형성은 객체 지향 프로그래밍의 강력한 기능 중 하나로, 프로그램의 유연성과 확장성을 크게 향상시킵니다. 이 개념을 이해하고 적절히 활용하면, 더욱 효율적이고 유지보수가 용이한 코드를 작성할 수 있습니다.

인터페이스(Interface)에 대한 설명과 예제를 준비했습니다. 인터페이스는 자바에서 중요한 개념 중 하나로, 클래스의 설계를 보다 유연하게 만들어 주는 역할을 합니다.

# 인터페이스

## (1) 인터페이스란?
인터페이스는 모든 메소드가 추상 메소드로 선언되는 특별한 형태의 클래스입니다. 
인터페이스는 메소드의 시그니처(이름, 매개변수 목록, 반환 타입)를 정의하지만, 
메소드의 구체적인 구현은 인터페이스를 구현하는 클래스에서 담당합니다.

## (2) 인터페이스의 특징
- **추상 메소드**: 인터페이스에 선언된 모든 메소드는 기본적으로 추상 메소드입니다.
- **구현의 분리**: 인터페이스를 사용하면 구현을 분리시켜, 코드의 유연성과 확장성을 높일 수 있습니다.
- **다중 상속**: 인터페이스를 통해 자바에서 다중 상속과 유사한 효과를 얻을 수 있습니다.
- **기본 메소드와 정적 메소드**: 자바 8부터 인터페이스에 기본 메소드(default method)와 정적 메소드(static method)를 선언할 수 있습니다.

## (3) 인터페이스의 주요 사용처
- **다형성의 활용**: 인터페이스를 사용하여 다형성을 구현할 수 있습니다. 예를 들어, 여러 클래스가 같은 인터페이스를 구현하면 이 인터페이스 타입으로 여러 객체를 참조할 수 있습니다.
- **API의 정의**: 인터페이스를 통해 공개 API를 정의하고, 구체적인 구현은 API 사용자에게 위임할 수 있습니다.
- **모듈 간 결합도 감소**: 인터페이스를 통해 구현체와 사용처 간의 결합도를 낮출 수 있어, 시스템의 유연성과 확장성을 높일 수 있습니다.

## 예제: 인터페이스

```java
public class Main {
    public static void main(String[] args) {
        // 인터페이스를 구현한 클래스의 객체 생성
        Movable car = new Car();
        car.move();

        Movable bicycle = new Bicycle();
        bicycle.move();
    }
}

// 인터페이스 선언
interface Movable {
    void move();
}

// 인터페이스 구현
class Car implements Movable {
    @Override
    public void move() {
        System.out.println("자동차가 움직입니다.");
    }
}

class Bicycle implements Movable {
    @Override
    public void move() {
        System.out.println("자전거가 움직입니다.");
    }
}
```

이 예제에서 `Movable` 인터페이스는 `move` 메소드를 선언하고, `Car`와 `Bicycle` 클래스는 `Movable` 인터페이스를 구현합니다. 인터페이스를 구현하는 클래스는 인터페이스에 선언된 모든 추상 메소드를 구현해야 합니다.

인터페이스는 객체 지향 프로그래밍의 중요한 원칙인 '프로그래밍에서의 인터페이스와 구현의 분리'를 실현하는 데 도움을 줍니다. 이를 통해 더 유연하고, 확장 가능하며, 유지보수가 용이한 코드를 작성할 수 있습니다.

인터페이스에서 사용되는 추상 메소드, 기본 메소드, 정적 메소드에 대해 설명하겠습니다. 이 내용을 블로그의 메소드 부분에 추가할 수 있습니다.

## (4) 인터페이스 메소드

### (4-1) 추상 메소드
- **정의**: 추상 메소드는 선언만 되어 있고, 구현은 되어 있지 않은 메소드입니다.
- **특징**: 추상 메소드는 메소드 본문이 없으며, 세미콜론(`;`)으로 끝납니다.
- **사용**: 추상 메소드는 주로 인터페이스 또는 추상 클래스 내에 선언됩니다.

#### 예제: 추상 메소드
```java
interface Movable {
    void move(); // 추상 메소드
}
```

### (4-2) 기본 메소드
- **정의**: 자바 8부터 인터페이스에 도입된 기본 메소드는 인터페이스 내에서 `default` 키워드로 선언되며, 본문을 가진 메소드입니다.
- **목적**: 기존 인터페이스를 수정할 때 기존 구현 클래스에 영향을 주지 않으면서 새로운 기능을 추가할 수 있습니다.

#### 예제: 기본 메소드
```java
interface Movable {
    void move(); // 추상 메소드

    default void stop() { // 기본 메소드
        System.out.println("정지합니다.");
    }
}
```

### (4-3) 정적 메소드
- **정의**: 자바 8부터 인터페이스에 도입된 정적 메소드는 `static` 키워드를 사용하여 선언되며, 인터페이스 이름으로 직접 호출됩니다.
- **사용**: 정적 메소드는 유틸리티 함수나 인터페이스와 관련된 도우미 함수를 제공하는 데 사용됩니다.

#### 예제: 정적 메소드
```java
interface Movable {
    static void printSpeed(int speed) { // 정적 메소드
        System.out.println("속도: " + speed);
    }
}
```

### (4-4) 메소드 요약
- **추상 메소드**: 구현되지 않은 메소드, 서브클래스에서 반드시 구현해야 합니다.
- **기본 메소드**: 인터페이스 내에서 구현된 메소드, 모든 구현 클래스에서 상속됩니다.
- **정적 메소드**: 인터페이스에 바인딩된, 인스턴스 생성 없이 호출할 수 있는 메소드입니다.

추상 클래스(Abstract Class)에 대한 설명과 예제를 준비했습니다. 이 내용은 블로그의 추상 클래스 부분에 추가되어 독자들이 이 중요한 개념을 이해하는 데 도움이 될 것입니다.

# 추상 클래스 

## (1) 추상 클래스란?
- **정의**: 추상 클래스는 하나 이상의 추상 메소드를 포함하거나, `abstract` 키워드로 정의된 클래스입니다.
- **목적**: 추상 클래스는 완전하지 않은 클래스로서, 상속을 통해 자식 클래스에서 완성되도록 설계됩니다.
- **사용**: 추상 클래스는 인스턴스화할 수 없으며, 상속을 통해 서브 클래스에서 확장해야 합니다.

## (2) 추상 클래스의 특징
- **추상 메소드와 일반 메소드**: 추상 클래스는 추상 메소드뿐만 아니라 일반 메소드도 포함할 수 있습니다.
- **생성자**: 추상 클래스는 생성자를 가질 수 있으며, 이는 서브 클래스의 생성자에서 호출될 때 사용됩니다.
- **상속**: 추상 클래스를 상속받은 서브 클래스는 모든 추상 메소드를 구현해야 합니다.

## (3) 추상 클래스의 주요 사용처
- **공통 기능의 정의와 확장**: 공통 기능을 추상 클래스에 정의하고, 다양한 방식으로 이를 확장할 수 있습니다.
- **템플릿 메소드 패턴**: 추상 클래스에서 알고리즘의 구조를 정의하고, 서브 클래스에서 알고리즘의 특정 단계를 구현하는 방식으로 사용됩니다.

## 예제: 추상 클래스

```java
public class Main {
    public static void main(String[] args) {
        // 추상 클래스의 서브 클래스 인스턴스화
        Animal cat = new Cat();
        cat.sound();

        Animal dog = new Dog();
        dog.sound();
    }
}

// 추상 클래스 선언
abstract class Animal {
    // 추상 메소드
    abstract void sound();

    // 일반 메소드
    void breathe() {
        System.out.println("숨을 쉽니다.");
    }
}

// 추상 클래스를 상속받는 서브 클래스
class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("야옹");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("멍멍");
    }
}
```

이 예제에서 `Animal`은 추상 클래스이며, `sound()` 메소드는 추상 메소드입니다. `Cat`과 `Dog` 클래스는 `Animal` 클래스를 상속받아 `sound()` 메소드를 각각 구현합니다.

추상 클래스는 객체 지향 프로그래밍에서 중요한 역할을 하며, 코드의 재사용성과 확장성을 향상시킵니다. 추상 클래스를 이해하고 올바르게 사용하면, 유지보수가 용이하고 확장 가능한 프로그램을 설계할 수 있습니다.
