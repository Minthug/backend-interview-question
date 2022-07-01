# 간단한 AOP 설명
AOP는 Aspect Oriented Programming의 약자로 OOP 와 같은 프로그래밍 
패러다임의 하나이다,
"OOP와 상충되는 의미가 아닌 OOP를 돕는 프로그래밍 패러다임이다."
AOP란 횡단 관심사를 분리함으로써 모듈성을 증가시키는 것이 목적인 
프로그램이다

여기서 횡단 관심사란?

어플리케이션의 핵심 기능은 아니지만, 어플리케이션을 구성한 중요한 요소임과 
동시에 부가적인 기능을 담당하는 것
예시) 트랜잭션, 로깅, 성능 분석 등

```java
public class Car {
	private int speed;
    
	public void accelerate() {
		System.out.println("accelerate 실행");
	    this.speed += 10;
    	System.out.println("accelerate 종료");
    }
    public void breakCar() {
    System.out.println("breakCar 실행");
    this.speed = 0;
    System.out.println("breakCar 종료");
    }
  }  
    
```
해당 코드를 보면 부가기능 <code>log 출력</code>가 여러 곳에 위치한것을 볼 
수 있다.

부가기능의 입장에서 바라보면 중복되는 코드를 찾을 수 있는데, AOP는 기존의 
OOP에서 바라보던 관점을 부가기능의 입장에서 보았을 때, 공통적인 요소들을 
따로 모듈화 하는 것이다

코드가 핵심코드(핵심 관심사) + 부가기능(횡단 관심사) 으로 이루어져 있다고 
볼때, 반복되는 부가기능을 핵심코드로 부터 분리하는 것이 AOP의 핵심이다

# AOP가 왜 필요한지?
AOP가 없어도 프로그래밍은 가능할 것이다.
하지만 프로그래밍을 하다보면 공통적인 기능이 많이 발생한다.
간단한 예로 메소드가 실행되는지를 확인하기 위해 메서드 실행 전후로 Log를 
출력하는 등의 기능이 있다.

이런 코드를 계속 작성하면 OOP를 방해하게 된다, 따라서 이런 문제를 해결하기 
위해 Spring에선 AOP를 지원하는 것이다

## OOP를 방해한다는 것은 무엇을 의미하는가?

```java
public class Car {
	private int speed;
    
    public void accelerate() {
    	this.speed += 10;
        }
        
    public void breakCar() {
    	this.speed = 0;
        }
    }
```    

**OOP** 에선 Car 라는 클래스가 있을때 Car Class 는 Car와 관련된 행위 및 
속성만 존재해야하며, 해당 클래스의 목적과 관련되지 않는 것들은 제외 시켜야 
한다.

```java
public class Car {
	private int speed;
    
	public void accelerate() {
		System.out.println("accelerate 실행");
	    this.speed += 10;
    	System.out.println("accelerate 종료");
    }
    public void breakCar() {
    System.out.println("breakCar 실행");
    this.speed = 0;
    System.out.println("breakCar 종료");
    }
  }  
    
```
이 코드는 어떠한가? 로그를 출력하기위해 코드를 변경하였다.
Log를 출력하는 기능은 Car 클래스와는 관련이 없지만 Car 클래스 안에 로그를 
출력하기 위한 코드를 기술함으로써 해당 객체와 관련이 없는 코드가 추가되어 
추상화를 방해하게 된다.

## OOP의 목적 : 코드의 재사용성 && 중복제거
이렇게 코드에 로그 출력하는 코드가 계속해서 반복되며 중복을 일으키고, 만약 
특정한 조건에 로그를 출력하는 코드가 기입된다면 해당 코드를 재사용하기도 
어렵게 될 것이다.

### 그럼 AOP가 아닌 상속으로 진행하면 되지 않을까?

상속을 한다면 Log 출력 코드를 해당 클래스에 넣지 않고 로그 기능이 필요한 
클래스에서만 상속하여 사용할 수 있을 것이다.
물론, 가능할 것이다!
하지만 자바에선 다중상속을 지원하지 않기 때문에 좋지 못할 뿐더러, 상속의 
목적에 맞지 않는다.
상속은 **'어떤 클래스를 확장할 목적'** 가지고 있다, 따라서 상속을 이용해 
로그를 출력하면 코드의 가독성을 떨어뜨리고 좋지못한 설계가 될 것이다

## 코드가 1000개가 넘을땐?
상속으로 진행하고 그냥 일일이 수정할 수 있다!
물론 그 수가 10개도 안되고 짧은 코드로 작성이 가능할 때 말이다.
하지만 이렇게 극단적으로 1000개가 넘는 코드를 다 수정하려고하면, 개발자는 
모든 코드를 하나하나 살펴가며 수정을 진행 해야할 것이다.
할 수는 있겠지만, 시간과 정신력이 금방 바닥을 칠 것이다.

# 결론
로그, 시간측정 하는 기능은 핵심 기능이 아니다.
이건 핵심 기능이 아닌 공통 관심 사항이다 !
로그를 출력하는 기능 및 시간 측정 등이 핵심 비즈니스 로직과 섞여서 
유지보수가 굉장히 어려워진다.

```java
public class LogAop {
	public Object logging(ProceedingJoinPoint joinPoint) throws 
Throwable {
    	String methodName = joinPoint.getSignature().toShortString();
        System.out.println(methodName + "is Start. " );
        
        try {
        	Object obj = joinPoint.proceed();
            return onj;
       } finally {
       		System.out.println(methodName + " is Finish. ")
            }
       }
  }     
```
logging method의 첫줄에서 인자로 받아온 joinPoint를 이용해 메서드의 이름을 
받아오고
try문 안의 joinPoint.proceed() 메서드의 경우 핵심관심사를 실행하도록 하는 
메서드이다
logging 메서드는 부가기능을 실행한 후 -> 핵심기능을 실행한다 -> 부가기능을 
실행한다.

