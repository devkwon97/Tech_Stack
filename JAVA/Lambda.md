## 람다 표현식(Lambda Expression)

### 1.람다식이란?
람다식은 메서드를 하나의 식으로 표현한 것.
```
- 객체 지향 언어보다는 함수 지향 언어에 가깝다.  
- 함수를 간략하면서도 명확한 식으로 표현할 수 있도록 해준다.  
- 메서드를 람다식으로 표현하면 메서드의 이름 및 반환 값이 없어지므로 익명 함수 라고도 한다.  
- 람다식의 형태는 매개 변수를 가진 코드 블록이지만 런타임 시에는 익명 구현 객체를 생성한다.  
```

람다식 사용
```
(매개변수, ...) -> { 실행문 ... }
```
(매개변수, ...)는 오른쪽 중괄호 { } 블록을 실행하기 위해 필요한 값을 제공하는 역할.  
-> 기호는 매개 변수를 이용해서 중괄호 { } 바디를 실행한다는 뜻으로 해석.

```
interface ExFunctionInterface
{
    public void method();
}

public class ExFunctionInterfaceTest
{
    public static void main(String[] args)
    {
        ExFunctionInterface test = new ExFunctionInterface() {

            public void method() {
                System.out.println("test");
            }
        };

        test.method();
    }
}

// Lambda 적용
public class ExFunctionInterfaceTest
{
    public static void main(String[] args)
    {
        ExFunctionInterface test = () -> System.out.println("test");

        test.method();
    }
}

```

* 반환 값이 있는 메서드의 경우 return 대신 expression 으로 대신할 수 있다.
 (expression인 경우 ; 를 붙이지 않는다.)
* 람다식에 선언된 매개변수 타입은 추론이 가능한 경우 생략 가능 (대부분 생략가능)
* 매개 변수가 하나인 경우 ()를 생략할 수 있다.
* {} 안 문장이 하나인 경우 생략할 수 있다.
