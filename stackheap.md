# Stack & Heap

# Stack

- Heap 영역에 생성된 Object 타입의 데이터의 참조값이 할당된다.
- 원시타입의 데이터가 값과 함께 할당된다.
- 지역변수들은 scope 에 따른 visibility 를 가진다.
- 각 Thread 는 자신만의 stack 을 가진다.

![image](/uploads/ea45091550926ba8c3649c697dc34544/image.png)

#include <stdio.h>

void fct1(int); 
void fct2(int); 

int a = 10; // 데이터 영역에 할당 
int b = 20; // 데이터 영역에 할당 

int main() { 
    int i = 100; // 지역변수 i가 스택 영역에 할당 
    fct1(i); 
    fct2(i); 
    return 0; 
} 

void fct1(int c) { 
    int d = 30; // 매개변수 c와 지역변수 d가 스택영역에 할당 
} 

void fct2(int e) {
    int f = 40; // 매개변수 e와 지역변수 f가 스택영역에 할당 
}

![image](/uploads/8d87f27d6ce9eb20fa9cbb2d25cf73ee/image.png)


# Heap

- Heap 영역에는 주로 긴 생명주기를 가지는 데이터들이 저장된다. (대부분의 오브젝트는 크기가 크고, 서로 다른 코드블럭에서 공유되는 경우가 많다)

- 애플리케이션의 모든 메모리 중 stack 에 있는 데이터를 제외한 부분이라고 보면 된다.

- 모든 Object 타입(Integer, String, ArrayList, ...)은 heap 영역에 생성된다.

- 몇개의 스레드가 존재하든 상관없이 단 하나의 heap 영역만 존재한다.

- Heap 영역에 있는 오브젝트들을 가리키는 레퍼런스 변수가 stack 에 올라가게 된다.


![image](/uploads/6c4239f377dc4e505bb6c1a43605c7e5/image.png)

![image](/uploads/667a35198a3b98d963bd362079eb5f49/image.png)

