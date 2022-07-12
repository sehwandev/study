# [팩토리 패턴(factory pattern)](https://jusungpark.tistory.com/14)
- *팩토리 메서드 패턴* : 객체를 생성하기 위한 인터페이스를 정의하는데, 어떤 클래스의 인스턴스를 만들지는 서브클래스에서 결정하게 만듦. 즉 팩토리 메서드 패턴을 이용하면 클래스의 인스턴스 만드는 일을 서브클래스에게 맡김.
- *추상 팩토리 패턴* : 인터페이스를 이용하여 서로 연관된, 또는 의존하는 객체를 구상 클래스를 지정하지 않고도 생성.

```typescript 
new
```
위와 같은 키워드를 사용하는 것은 구상 클래스(*Concrete Class*: 클래스 내의 모든 메서드가 구현되어 있어야함)의 인스턴스를 만드는 것이다. -> 인터페이스가 아닌 특정 구현을 사용함.

- 구상 클래스가 있는 경우의 코드
```typescript
if(type == picnic) duck = new MalardDuck();
else if(type == hunting) duck = new DecoyDuck();
else if(type == inBathTub) duck = new RubberDuck();
```
변경하거나 확장해야 할 코드를 다시 확인하고 추가 혹은 제거해야함.

인터페이스에 맞춰서 코딩하면 시스템에서 일어나는 여러 변화를 이겨낼 수 있음 -> 다형성 덕분에 어떤 클래스든 특정 인터페이스만 구현하면 사용 가능
