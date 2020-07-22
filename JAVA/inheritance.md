## 상속

### 1.상속의 정의와 장점
상속이란 기존의 클래스를 재사용하여 새로운 클래스를 작성 하는 것이다.  
상속을 톨해 적은양으로 코딩 할수 있고 공통적으로 관리하여 유지보수에 용이하다.

### 2.클래스간의 관계 - 포함관계
상속이에외에도 클래스를 재사용 하는 방법은 클래스간의 `포함(Composite)` 관계를 맺어주는 것이다.  
클래스 간의 포함관계를 맺어주는 것은 한 클래스의 멤버변수로 다른 클래스 타입의 참조변수를 선언하는 것을 뜻한다.

```
class Circle {
    int x;  // 원점의 x좌표
    int y;  // 원점의 y좌표
    int r;  // 반지름(radius)
}

class Point {
    int x;  // 원점의 x좌표
    int y;  // 원점의 y좌표
}
```
Point 클래스 재사용으로 Circle 클래스 작성
```
class Circle {
    Point c = new Point(); // 원점
    int r;
}
```

### 3. 클래스간의 관계 결정하기
```
상속관계 : '~은 ~이다 (is-a)'
포함관계 : '~은 ~을 가지고 있다 (has-a)'
```