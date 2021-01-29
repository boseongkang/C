## C++

<hr>

C++의 실행방식은 C언어와 동일하다. 한가지 차이점은 컴파일할때 확장자를 .c가 아닌 .cpp로 설정 해주어야 한다. 

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