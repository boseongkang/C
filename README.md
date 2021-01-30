## C++

<hr>
C++의 실행방식은 C언어와 동일하다. 한가지 차이점은 컴파일할때 확장자를 .c가 아닌 .cpp로 설정 해주어야 한다. 

### 1-1 입, 출력 방식

<hr>

**특징 1 :** C 언어에서는 코드 작성시 제일 상단에 `#include <stdio.h>` 라는 헤더파일을 작성해야 했는데 C++은  생략한다. 

#### Hello World C++로 출력

```c++
#include <iostream>

int main(void) {
	std::cout << "Hello World!" << std::endl;
	std::cout << "Hello " << "World!" << std::endl;
	return 0;
}
```

**특징 2 :** C++언어는 출력할때 `std::cout << 변수;` 이 형식이 기본이다. 아직 공부하는 중이라 std와 cout의 의미가 무엇인지는 모르겠다. std::endl은 `\n` 이 개행처리 해주는 문자와 같다. 

**특징 3 :** `<<` 이것도 연산자다. `std::cout << "Hello " << "World!" << std::endl;` 연산자를 활용하여 Hello World! 를 출력할 수 있다. 

**특징 4 :** C언어의 scanf, Java의 scanner와 같은 문법이 C++에서는 `std::cin >> 변수;` 이다. 
			 `std::cin >> 변수1 >> 변수2;` 구조로 연속적으로 값을 입력 받을 수 있다. 

**특징 5 :** 지역변수(local variable) 선언이 함수 내 어디서든 가능하다.

<hr>

### 1-2 함수 오버로딩

C언어 에서는 동일 이름의 함수 정의가 불가했지만 C++은 가능하다. 

함수 호출시 전달되는 인자를 통해 호출하고자 하는 함수를 구분하기때문. 

**특징1 : ** 매개변수(parameter)의 선언이 달라야 한다. 즉, 자료형이 달라야 한다. 

**특징 2 : ** 매개변수의 갯수가 달라야한다. 

<hr>

### 1-3 매개변수의 기본 값

```c++
int MyFunc(int num=1){
    return 0;
}
```

이러한 형태로 선언 가능하다.

함수호출 시 매개변수를 전달하지 않으면 1의 값을 전달하겠다. 로 이해하면 된다. 

**특징1 : ** default 값은 함수의 선언 부분에만 표현하면 된다. 

**특징2 : ** 매개변수의 default값을 선언할때 오른쪽 매개변수부터 채워야 한다. 

1. ##### `int MyFunc(int num1, int num2, int num3 = 10){}` (O)

2. ##### `int MyFunc(int num1=10, int num2, int num3){}` (X)

3. ##### `int MyFunc(int num1=10, int num2,=20 int num3){}` (X)

<hr>