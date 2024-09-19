# Backend-Interview-Question


Table Of Contents
---------------

- 네트워크
- 정규화
- CS 관련지식
- 언어 관련
- 면접 관련 추천 영상
---------------------
# CS 관련 지식

#운영체제

#프로세스
<details>
<summary>프로세스와 스레드의 차이는 무엇인가요?</summary>

프로세스는 독립적인 실행 단위로, 각각 별도의 메모리 공간을 가집니다.
반면 스레드는 하나의 프로세스내에서 실행되며 같은 프로세스의 메모리를 공유합니다.

프로세스는 서로 독립적이어서 한 프로세스의 문제가 다른 프로세스의 영향을 주지 않습니다.
하지만 같은 프로세스내의 스레드들은 서로 영향을 줄 수 있습니다.

프로세스는 생성과 컨텍스트 스위칭에 더 많은 오버헤드가 발생하지만, 스레드는 상대적으로 가볍고 빠릅니다.

</details>

<details>
<summary>교착상태란 무엇이며, 교착상태가 발생하기 위해서는 어떤 조건이 있어야 하나요?</summary>

자바
</details>

<details>
<summary>교착상태의 해결법은 무엇인가요?</summary>

자바
</details>

<details>
<summary>뮤텍스와 세마포어에 대해서 설명해 보시오.</summary>

자바
</details>

<details>
<summary>컨텍스트 스위칭이란 무엇인가요?</summary>

자바
</details>

<details>
<summary>경쟁 상태란 무엇인가요?</summary>

자바
</details>

<details>
<summary>프로세스 혹은 스레드의 동기화란 무엇인가요?</summary>

자바
</details>

<details>
<summary>사용자 수준의 스레드와 커널 수준의 스레드의 차이는 무엇인가요?</summary>

자바
</details>

<details>
<summary>CPU 스케줄링이란 무엇인가요?</summary>

자바
</details>

<details>
<summary>CPU 스케줄링 방법에는 대표적으로 어떤 것들이 있나요?</summary>

자바
</details>

<details>
<summary>동기와 비동기, 블로킹과 넌블로킹의 차이는 무엇인가요?</summary>

동기는 작업을 순차적으로 실행하며, 한 작업이 완료될 떄까지 다른 작업을 시작하지 않습니다.
비동기는 작업을 시작한 후 완료를 기다리지 않고 다른 작업을 진행합니다, 작업 완료 시 콜백, 프로미스 등으로 처리합니다.

블로킹은 작업이 완료될 때까지 제어권을 가지고 대기합니다.
논블로킹은 작업 완료 여부와 관계없이 즉시 제어권을 반환합니다.

주요 차이는 동기/비동기는 작업 순서와 흐름 제어에 관한것이고,
블로킹/논블로킹은 작업의 제어권 반환 여부에 관한 것 입니다.

</details>

# 메모리

<details>
<summary>프로세스에 할당되는 메모리의 각 영역에 대해서 설명해 주세요</summary>

자바
</details>

<details>
<summary>메모리 구조의 순서가 어떻게 되는가? CPU에서 가까운 순으로 말해보시오.</summary>

자바
</details>


<details>
<summary>페이지와 세그멘테이션에 대해서 설명해 보시오.</summary>


</details>



<details>
<summary>외부 단편화란? 내부 단편화란?</summary>

자바
</details>



<details>
<summary>First Fit, Best Fit, Worst Fit에 대해서 설명해 보시오.</summary>

자바
</details>



<details>
<summary>페이지 교체 알고리즘 종류에는 어떤 것들이 있나요?</summary>

자바
</details>

#네트워크
## 전산 기본

<details>
<summary>OSI 7계층에 대해서 설명해주세요.</summary>

자바
</details>



<details>
<summary>TCP/IP 4계층에 대해서 설명해주세요.</summary>

자바
</details>



<details>
<summary>DNS가 무엇인가요?</summary>

자바
</details>



<details>
<summary>도메인 이름으로 실제 IP를 어떻게 찾을 수 있는지 흐름을 설명해 주세요.</summary>

자바
</details>


# TCP/UDP

<details>
<summary>TCP와 UDP의 차이에 대해서 설명해 주세요.</summary>

자바
</details>



<details>
<summary>TCP 헤더에 대해서 설명해 주세요.</summary>

자바
</details>



<details>
<summary>MTU가 무엇인가요?</summary>

자바
</details>



<details>
<summary>3-way hand shake, 4-way hand shake 흐름에 대해서 설명해주세요.</summary>

자바
</details>

#HTTP

<details>
<summary>HTTP 프로토콜에 대해서 아는대로 말해주세요.</summary>
웹에서 서버와 클라이언트간의 데이터를 주고받는 모델의 프로토콜입니다.
요약하면 웹브라우저가 서버와 통신하는 규칙입니다.
</details>

<details>
<summary>HTTP와 HTTPS 의 차이는 무엇인가요?</summary>

HTTP는 암호화 되지 않은 평문 통신이고, HTTPS는SSL/TLS를 통해 암호화된 보안 통신입니다.
또한 HTTP는 80 포트이고 HTTPS는 443 입니다.
물론 핵심은 HTTPS는HTTP에 보안계층을 추가한 프로토콜로 데이터의 안전한 전송을 보장합니다.

아주 쉽게 말하면 HTTP는 웹브라우저가 서버와 통신하는 규칙이고 HTTPS는 데이터 암호화가 추가된 프로토콜인것이다.

</details>

<details>
<summary>HTTPS가 동작하는 방식에 대해서 설명해 주세요.</summary>
HTTPS는 클라이언트가 서버에 연결을 시작하면 서버에서 SSL/TLS 인증 과정을 거치는데,
이때 공개키와 디지털 인증서를 클라이언트에게 전송합니다.
클라이언트는 세션키를 생성하고 세션키를 서버에게 받은 공개키로 암호화하여 다시 서버에게 전송합니다.
서버는 개인키로 암호화된 세션키를 복호화하고 저장합니다.
이 후부터는 클라이언트와 서버간의 동일한 세션키를 가지고 안전하게 통신을 합니다.


</details>

<details>
<summary>HTTP 1.0과 1.1의 차이는 무엇인가요?</summary>

자바
</details>

<details>
<summary>HTTP2와 그 특징에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>HTTP 헤더의 구조에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>keep-alive 헤더에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>HTTP GET과 POST의 차이는 무엇인가요?</summary>

자바
</details>

<details>
<summary>쿠키와 세션에 대해서 설명해 주세요.</summary>

쿠키는 웹 서버가 사용자의 웹 브라우저에 저장하는 작은 텍스트 파일입니다.
세션은 서버측에서 유지되는 사용자별 상태 정보입니다.

쿠키는 클라이언트측에게 저장되고 세션은 서버측에 저장됩니다

대게 쿠키는 방문 사이트 로그인 시 아이디, 비밀번호 저장에 사용하거나 쇼핑몰의 장바구니 기능 등에서
쉽게 접할 수 있습니다

세션은 쿠키를 기반으로 만들어져있지만 보안 측에서 더 우수합니다
또한 서버에서 관리하는 만큼 로그인같이 보안상 중요한 작업을 수행할 때 사용합니다.


</details>

# WEB (웹)

<details>
<summary>웹브라우저에서 서버로 요청했을 때, 흐름을 설명해주세요.</summary>

자바
</details>

<details>
<summary>CORS란 무엇인가요?</summary>

CORS는 도메인이 다른 서버끼리 리소스를 주고 받을 때 보안을 위해 설정된 정책입니다.

또한 CORS가 다른 도메인을 구분하는 동일 오리진 정책은 URL에서 프로토콜, 호스트, 포트로 구분합니다.

</details>

<details>
<summary>웹 서버와 웹 어플리케이션 서버(WAS)의 차이는 무엇인가요?</summary>

자바
</details>

<details>
<summary>REST API에 대해서 설명해 주세요.</summary>

REST API는 REST의 원리를 따르는 API를 의미합니다.
URI는 동사보다 명사를 대문자보단 소문자를 사용한다
마지막에 슬래시를 포함하지 않는다.
언더바 대신 하이픈을 사용한다
파일확장자는 URI에 포함하지 않는다.
행위를 포함하지 않는다
이 규칙을 지키면서 설계하는 것을 말합니다.
 
</details>

<details>
<summary>API Gateway란 무엇인가요?</summary>

자바
</details>

<details>
<summary>API Gateway가 다운되면 모든 API를 사용 못할지도 모르는데, 어떤 방안을 마련해야 할까요?</summary>

자바
</details>

# 데이터베이스
## 전산 기본
<details>
<summary>JOIN에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>내부 조인과 외부 조인의 차이는 무엇인가요?</summary>

자바
</details>

<details>
<summary>정규화에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>파티셔닝과 샤딩에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>ORM이란 무엇인가요?</summary>

객체 관계 매핑 입니다.
객체와 관계형 데이터베이스의 데이터를 자동으로 매핑해주는 역할을 합니다.

</details>

<details>
<summary>NoSQL이란 무엇인가요?</summary>
Non-relational SQL 의 약자로 
전통적인 관계형 데이터 베이스와는 다른 접근 방식을 사용하는 데이터 베이스 시스템 입니다.

또한 특징은 스키마가 없고 수평적 확장성과 고성능이 있고 다양한 데이터 모델이 있습니다.

대표적으로 Redis, MongoDB 등이 있습니다.

</details>

<details>
<summary>스키마란 무엇인가요?</summary>
스키마는 데이터베이스의 구조와 제약조건에 관한 전반적인 기술 명세를 기술한 것입니다.
간단히 데이터베이스에서 데이터가 구성되는 방식과 서로 간의 관계를 정의한 것인데

테이블/필드/데이터 타입/제약조건/관계 의 구성요소로 이루어져있습니다.

</details>

## 인덱스

<details>
<summary></summary>

자바
</details>

<details>
<summary>인덱스란 무엇인가요? 어떻게 동작 하나요?</summary>

자바
</details>

<details>
<summary>인덱스의 알고리즘에는 어떤 것들이 있나요?</summary>

자바
</details>

<details>
<summary>Table Full Scan과 Index Range Scan 을 설명해주세요.</summary>

자바
</details>

# 트랜잭션

<details>
<summary>트랜잭션이란 무엇인가요? 4가지 원칙을 포함해서 설명해 주세요.</summary>
트랜잭션은 데이터베이스의 상태를 변화시키기 위해 수행하는 작업의 단위입니다.
또한 4가지의 특성을 가지고 있습니다
첫재로 원자성인데 트랜잭션의 모든 연산이 완전히 수행되거나, 전혀 수행되지 않아야합니다.
그다음 일관성은 트랜잭션 실행 전과 후의 데이터베이스는 일관된 상태를 유지해야합니다.
격리성은 동시에 실행되는 트랜잭션들이 서로 영향을 미치지 않아야합니다.
지속성은 성공적으로 완료된 트랜잭션의 결과는 영구적으로 반영되어야 합니다.

 </details>

<details>
<summary>트랜잭션의 격리 수준과 각 수준에서 발생할 수 있는 문제들에 대해 말해보세요.</summary>

자바
</details>

<details>
<summary>공유 락과 배타 락의 차이는 무엇인가요?</summary>

자바
</details>

<details>
<summary>데드락이란 무엇이며, 어떻게 발생할까요?</summary>

자바
</details>

<details>
<summary> ≈y</summary>

</details>



# 알고리즘
## 전산 기본

<details>
<summary>빅오 표기법에 대해서 설명해주세요</summary>

자바
</details>

<details>
<summary>팩토리얼(factorial)을 구현해 보세요(손코딩).</summary>

자바
</details>

<details>
<summary>피보나치 수열 구현 방식 세 가지를 말해보시고, 시간복잡도와 공간복잡도를 설명해 주세요.</summary>

자바
</details>

<details>
<summary>BFS/DFS 차이는 무엇인가요?</summary>

자바
</details>

<details>
<summary>프림 알고리즘에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>다익스트라 알고리즘에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>은행원 알고리즘에 대해서 설명해 주세요.</summary>

자바
</details>

## 정렬

<details>
<summary>정렬의 종류에는 어떤 것들이 있나요?</summary>
삽입, 선택, 버블, 퀵, 병합, 힙, 계수, 기수 정렬이 있습니다.

</details>

<details>
<summary>삽입 정렬이 일어나는 과정을 설명해 보세요.</summary>
정렬된 부분과 정렬되지 않는 부분으론 나누고, 정렬되지 않는 원소를 정렬된 부분의 적절히 삽입합니다.

💡 적절한 상황: 거의 정렬된 데이터나 작은 규모의 데이터에 효율적
</details>

<details>
<summary>퀵 정렬이 일어나는 과정을 설명해 보세요.</summary>

피벗을 선택하고 작은 값과 큰 값으로 분할한 후 재귀적으로 정렬합니다.

💡 적절한 상황: 대규모 데이터에 매우 효율적이며 평균적으로 가장 빠른 정렬 알고리즘 입니다.
</details>

<details>
<summary>버블 정렬이 일어나는 과정을 설명해 보세요.</summary>
인접한 두 원소를 반복적으로 비교하여 큰 값을 뒤로 보냅니다 

💡 적절한 상황: 안정적인 정이 필요하거나 연결 리스트의 정렬에 효과적입니다.
</details>

<details>
<summary>선택 정렬이 일어나는 과정을 설명해 보세요.</summary>
전체에서 최솟값을 찾 맨 앞으로 이동 시키는 과정을 반복합니다.

💡 적절한 상황: 작은 규모에 데이터나 메모 사용이 제한적일 경우에 유용합니다.
</details>

<details>
<summary>힙 정렬이 일어나는 과정을 설명해 보세요.</summary>
데이터 최대 힙을 구성한 후, 루트를 꺼내어 맨 뒤로 보내는 과정을 반복합니다.
💡 적절한 상황: 최댓값/최솟값을 찾아야할 때나 메모리 사용이 제한적인 경우 유용합니다.
</details>

<details>
<summary>병합 정렬이 일어나는 과정을 설명해 보세요.</summary>
리스트를 반으로 나누고 각각을 정렬한 후 병합하는 과정을 재귀적으로 수행합니다.
💡 적절한 상황: 안정적인 정렬이 필요하거나 연결 리스트의 정렬에 효과적입니다.
</details>

<details>
<summary>계수 정렬이 일어나는 과정을 설명해 보세요.</summary>
각 원소의 출현 횟수를 세어 저장한 , 이를 기반으로 정렬합니다.

💡 적절한 상황: 정수나 정수로 표현 가능한 데이터의 범위가 작을 때 매우 효율적입니다.
</details>

<details>
<summary>기수 정렬이 일어나는 과정을 설명해 보세요.</summary>
각 자릿수 별로 버킷에 분배하고 수집하는 과정을 반복합니다 

💡 적절한 상황: 정수나 문자 같이 자릿수가 있을 데이터의 정렬에 효과적입니다.
</details>

<details>
<summary>54321 배열이 있을 때, 어떤 정렬을 사용하면 좋을까요?</summary>

자바
</details>

<details>
<summary>랜덤으로 배치된 배열이 있을때, 어떤 정렬을 사용하면 좋을까요?</summary>

자바
</details>

<details>
<summary>자릿수가 모두 같은 수가 담긴 배열이 있을 때, 어떤 정렬을 사용하면 좋을까요?</summary>

자바
</details>

# 자료구조
## 전산 기본

<details>
<summary>배열과 링크드 리스트의 차이점에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>스택과 큐에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>해시테이블에 대해서 설명해 주세요.</summary>

자바
</details>

## 트리

<details>
<summary>포화(Perfect) 이진트리, 완전(Complete) 이진트리, 정(Full) 이진트리의 차이점에 대해 각각 설명해주세요.</summary>

자바
</details>

<details>
<summary>그래프와 트리의 차이점에 대해서 설명해 주세요.</summary>

자바
</details>

<details>
<summary>힙 자료구조에 대해 설명해 주세요.</summary>

자바
</details>

<details>
<summary>힙의 삽입과 삭제는 어떻게 이루어지나요?</summary>

자바
</details>

<details>
<summary>레드 블랙 트리에 대해 설명해주세요.</summary>

자바
</details>

<details>
<summary>레드 블랙 트리의 삽입과 삭제 과정에 대해서 말해보세요.</summary>

자바
</details>

<details>
<summary>B-Tree에 대해서 설명해 주세요.</summary>

자바
</details>


<details>
<summary>최소 신장 트리에 대해서 설명해 주세요.</summary>

자바
</details>

# 프로그래밍
## 전산 기본

<details>
<summary>.</summary>

자바
</details>


---------------------

# 언어 관련
## Java

<details>
<summary>자바 데이터 타입 중 기본형과 참조형의 차이에 대해 
설명해주세요.</summary>

두 개의 데이터 타입의 차이점은 기본형은 실제 값을 직접 저장하며, int, double 과 같이 간단한 데이터 타입에 사용됩니다.
기본형은 스택 메모리에 저장되고 고정된 크기를 가집니다.

참조형은 객체의 주소를 저장하는 타입으로 클래스, 인터페이스, 배열등에 사용되는데 이들은 실제 객체를 힙 메모리에 저장되고,
스택에는 그 주소가 저장됩니다.

또한 기본형은 null값을 갖지못하지만 참조형은 가능합니다.
그리고 기본형은 메서드를 가질 수 없고, 참조형은 객체의 메서드를 호출할 수 있습니다.


</details>

<details>
<summary>클래스와 객체에 대해 설명해주세요.</summary>
클래스는 객체를 만들어내기 위한 설계도 혹은 틀이라 할 수 있고,
객체를 생성하는데 사용합니다

객체는 클래스를 기반으로 생성되며 객체는 고유의 이름과 상태, 행동을 갖습니다.

여기서 객체의 상태는 필드 행동은 메서드라고 표현합니다.
객체에 메모리가 할당되어 실제로 활용되는 실체는 인스턴스라 합니다.

</details>


<details>
<summary>생성자에 대해 설명해주세요</summary>
생성자는 객체가 생성될 때 자동으로 호출되는 특별한 메서드 입니다.
주로 객체의 초기화 작업을 담당하며 객체 생성시 필요한 데이터를 강제할 수 있고
오버로딩이 가능해 여러 개의 생성자도 정의할 수 있습니다

또한 객체 생성 시 new 키워드를 함께 호출합니다.


- df 
</details>


<details>
<summary> 메서드 오버라이딩과 메서드 오버로딩의 차이는 무엇인가요? 
</summary>

오버라이딩은 상위 클래스에 있는 메서드를 하위 클래스에서 재정의 하는 것을 말하고
오버로딩은 메서드의 매개변수나 타입을 변경하여 같은 이름의 메서드를 여러 개 정의하는 것입니다.

가장 큰 차이는 오버라이딩은 상속관계에서 발생하고 오버로딩은 한 클래스 내에서 여러 개의 메서드를 정의 하는 점에서 확인 할 수 있습니다.

</details>

<details>
<summary>자바의 메모리 영역에 대해 설명해주세요.</summary>

힙/ 메서드 / 스택 / 피시 레지스터 / 네이티브 메서드 스택으로 5개의 영역을 지니고 있습니다.
</details>


<details>
<summary>static 키워드에 대해 설명하고, static를 언제 사용해야 하는 지 
설명해주세요.</summary>

ex
</details>

<details>
<summary>자바 객체지향 프로그래밍(OOP)에 대해 설명해주세요.</summary>

프로그래밍에서 필요한 데이터를 추상화시켜 상태와 행위를 가진 객체로 만들고 그 객체간의 상호작용을 통해 로직을 구성하는 방법을 말합니다.

4개의 주요 특징도 갖고 있는데
캡슐화 상속 추상화 다형성이 있습니다
간단하게 캡슐화는 속성과 행위를 클래스로 묶는 것인데 데이터 보호와 은닉을 할 수 있습니다.

상속은 기존 클래스의 속성과 메서드를 새로운 클래스가 재사용하는 것이고
추상화는 복잡한 시스템에서 핵심적인 개념이나 기능을 간추리는 것이며
다형성은 같은 인터페이스나 메서드가 다른 구현을 가질 수 있는것을 말하는데 유연성과 확장성을 챙깁니다.


</details>

<details>
<summary>자바 접근 제어자의 특징과 종류에 대해서 설명해주세요. </summary>

접근 제어자는 public, private, protected, default가 있습니다.
퍼블릭은 모든 클래스에서 접근이 가능한 접근 제어자입니다.
프라이빗은 같은 클래스내에서만 접근이 가능한 접근 제어자입니다.
프로텍티드는 같은 패키지안의 모든 클래스와 다른 패키지의 하위 클래스에서 접근이 가능합니다.
디폴트는 같은 패키지안의 클래스에서만 접근이 가능합니다.

</details>

<details>
<summary>추상 클래스와 인터페이스의 차이는 무엇인가요? </summary>

같은 추상화인 인터페이스와 추상클래스의 다른 점은 추상 클래스는 클래스 간의 연관 관계를 구축하는 것에 초점을 둔다면 인터페이스는 클래스의 특정 동작을 정의하고 다양한 클래스에서 공통 기능을 구현하는 것에 초점을 두고 있습니다.


</details>

<details>
<summary>이너클래스의 장점에 대해 설명해주세요.</summary>

ex
</details>

<details>
<summary>OOP의 장점과 단점에 대해 설명해주세요.</summary>


</details>

<details>
<summary>List, Set, Map의 차이에 대해서 설명해주세요.</summary>

리스트는 순서가 있고 중복을 허용하고 셋은 순서가 없으며 중복 또한 허용하지 않습니다
맵은 키-값 쌍으로 데이터를 저장하는 구조입니다. 물론 순서와 중복이 없습니다.
</details>

<details>
<summary>컬렉션과 스트림의 차이에 대해서 설명해주세요.</summary>

ex
</details>

<details>
<summary>제네릭에 대해서 설명하고, 컬렉션 클래스에서 왜 제네릭을 사용하는 
지 설명해주세요.</summary>

ex
</details>

<details>
<summary>재귀 함수와 반복문의 차이점에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary> Stack과 Queue의 차이점에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary>인접 행렬과 인접 리스트의 차이점은 무엇인가요?</summary>

ex
</details>


<details>
<summary>탐욕(Greedy) 알고리즘을 사용하기 위해 성립해야 하는 조건에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary>이진 탐색 알고리즘(BST)이 데이터를 효율적으로 찾기 위해 탐색하는 과정을 설명해주세요.</summary>

ex
</details>


<details>
<summary> 웹 브라우저에서 CORS 이슈가 발생하는 원인은 무엇이며, 서버에서 어떻게 해결할 수 있나요?</summary>

ex
</details>


<details>
<summary>URL과 URI의 차이점이 무엇인가요?</summary>

ex
</details>


<details>
<summary>DNS의 정의와 DNS가 필요한 이유에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary>REST API란 무엇인가요?</summary>

ex
</details>


<details>
<summary>Client Side Rendering 과 Server Side Rendering 의 차이점에 대해서 설명해주세요.</summary>

ex
</details>


<details>
<summary>트랜잭션에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary>Foreign Key와 Primary Key에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary> IOC에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary>Spring에서 AOP가 필요한 이유에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary>스프링 컨테이너(Spring Container)에 대해 설명해주세요.</summary>

ex
</details>


<details>
<summary>DI(Dependency Injection)에 대한 설명과 해당 기술의 장점에 대해 설명해주세요.</summary>

ex
</details>

### ✔ 테스팅

`24번` - 기능 테스트, 통합 테스트, 슬라이스 테스트, 단위 테스트에 대해서 설명해 주세요.

`25번` - JUnit의 Assertion이 무엇을 의미하는지 설명해 주세요.

`26번` - Given - When - Then 패턴에 대해서 설명해 주세요.

`27번` - MockMvc를 이용해 Spring MVC의 API 엔드포인트인 Controller를 테스트하는 방법을 설명해 주세요.


<details>
<summary> Mock이 무엇인지 설명해 주세요. </summary>

Mock 이란

실제 객체를 만들기엔 비용과 시간이 많이 들거나 의존성이 길게 걸쳐져있어 제대로 구현하기가 어려울 경우, 가짜 객체를 만들어 사용하는데
이것을 Mock이라고 합니다

즉, 실제와 동일한 기능은 하진 않지만 대략 호출을 하면, 이런 결과 이런 기능을 할것이라고 알려주는 용도로 사용한다

목 객체가 필요한 경우는
테스트 작성을 위한 환경 구축이 어려울때
테스트가 특정 경우나 순간에 의존적인 경우
혹은 시간이 오래걸리는 경우에 필요하며

주의할점이 있는데
Mock을 사용할 경우 테스트 케이스 유지에 복잡성이 더해지기 때문에,
의존성이 적은 구조로 프로그래밍 해야하며
실제 객체로 작동을 해봤을때 예상한것처럼 정상 작동이 하지 않을 수도 있다 이유는 Mock은 실제 객체가 아닌 흉내만 내는 가짜 객체이기 떄문이다

Mock을 무분별하게 사용할경우 리팩토링에서 에러가 발생해
테스트에 대한 유지보수 비용이 크게 발생할 수 있다.

객체에 필요한 행동만 주의 깊게 만들어 Mock 객체를 형성하는 것이 바람직하다 불필요하면 상태 검증 테스트가 가능하다면 만들지 않는 것을 권장합니다

</details>

`29번` - Stub과 Stubbing이 무엇인지 설명해 주세요.

`30번` - Mockito가 무엇인지, Mockito의 역할에 대해서 설명해 주세요.

`31번` - @SpringBootTest와 @@WebMvcTest의 차이점을 설명해 주세요.

### ✔ API 문서화


<details>
<summary> Swagger와 Spring Rest Docs의 장단점을 설명해 주세요.</summary>

Swagger vs spring Rest Docs

스웨거의 장점
API를 테스트 해 볼 수 있는 화면을 제공한다
스웨거는 적용이 쉽지만 컨트롤러에 어노테이션을 추가하면된다

단점
어노테이션도 굉장히 많기때문에 가독성이 매우 떨어진다
가장 큰 문제는 실제로 동작하지 않을 수 도 있다.



레스트 독스
제품 코드에 영향이 없다
익숙하면 높은 가독성
변경에 따라 유지보수를 최신화할수 있고
테스트를 통과해야만 작성되어 신뢰성이 높다

단점은
적용하는 난이도가 상당하다

</details>

`33번` - Spring Rest Docs의 API 문서화 동작 방식에 대해서 설명해 주세요.

`34번` - Spring Boot 기반 애플리케이션을 빌드하는 방법에 대해서 설명해 주세요.

`35번` - Spring Boot 기반 애플리케이션 빌드 시, 주로 사용하는 프로파일(Profile)에 대해서 설명해 주세요.

`36번` - Spring Boot 애플리케이션 실행 파일을 배포하는 방법에 대해서 설명해 주세요.

- 전통적인 배포 방식
- 클라우드 서비스에 배포하는 방식

### ✔ 인증 / 보안

`1번` - 인증과 인가의 차이에 대해 설명해 주세요.

`2번` - 세션에 대해서 모르는 사람한테 설명하듯 간단하게 설명해 주세요.

세션이란 우리가 인터넷 쇼핑몰을 이용할때 장바구니와 비슷한 개념이라고 편하게 예를 드리겠습니다.
우리가 쇼핑몰에서 상품을 구매하기위해 장바구니에 담아두었을때, 뒤에서 서버도 장바구니에 보관을 할 것입니다.
그리고 또 다른 상품을 담았을때 세션이 만약 존재 하지않는다면
우리가 바로 전에 장바구니엠 찜해놓았던 상품은 사라지고 방금 새로 찜해놓은 상품만 장바구니 속에 있을것입니다.

이게 바로 세션의 역할인데 사용자의 원하는 요구 및 각각의 상태를 서버에서 저장하는 기술이며,

더 쉬운 예로 우리가 웹페이지에 로그인 했을때 세션이 없다면 계속 로그인이 유지 되지않아서,
우리는 계속 로그인을 해야하는 상황이 생길것입니다.

그리고 서버에서 저장하고있기에 인터넷을 사용하면서 들어본 ‘쿠키’ 보다 보안적으로 안전하여 우리의 개인 정보를 지키기 쉽습니다!


`3번` - 세션과 쿠키 그리고 토큰 인증 방식에 대해 설명해 주세요.

`4번` ****- 세션과 토큰 인증 방식 중 각각의 장단점을 말씀해 주세요.

`5번` - HTTP와 HTTPS 각각에 대해 설명하고 둘의 차이점을 말씀해 주세요.


`6번` - HTTPS의 동작 방식을 설명해 주세요.

`7번` - OAuth 2.0의 워크플로우에 대해서 설명해 주세요.

`8번` - Spring Security의 인증 처리 흐름에 대해 설명해 주세요.

`9번` - Spring Security의 인가 처리 흐름에 대해 설명해 주세요.

`10번` - Filter가 무엇인지 설명하고 Filter Chain의 동작에 대해 설명해 주세요.
HTTP 요청과 응답을 변경할 수 있는 재사용 가능한 코드이며,
서블릿 2.3 규약에 새롭게 추가되었다
필터는 객체의 형태로 존재하고 있으며 클라이언트로부터 오는 request 와 최종자원(서블릿) 사이에 위치하며 클라이언트의 요청 정보를 알맞게 변경할 수 있다
또한 필터는 최종 자원과 클라이언트로 가는 response 사이에 위치하여 최종 자원의 request 결과를 알맞게 변경할 수 있다

요약하자면 필터의 가장 큰 역할은 사용자 request를 검증하고 필요에 따라 데이터를 추가하거나 변조하는 것이라고 보면 된다


필터체인은 여러개의 필터가 모여서 하나의 체인을 형성할때 첫번째 필터가 변경하는 request정보는 클라이언트의 request정보가 되지만, 체인의 두번째 필터가 변경하는 요청정보는 첫번째 필터를 통해 변경된 요청정보가 된다.
즉 요청정보는 변경에 변경에 변경을 거듭하게됩니다
응답 정보의 경우도 요청정보와 비슷한 과정을 거치지만 차이점은 필터의 적용 순서가 요청과 반대입니다
 


### ✔ Cloud

`11번` - 사용해 본 클라우드 인프라 서비스에 대해 소개해 주세요.

`12번` - vmware와 같은 가상머신이랑 Docker가 무슨 차이가 있는지 설명해 주세요.

도커는 코드 및 종속성을 함께 패키징하는 애플리케이션 계층의 추상화라고 정의할 수 있습니다.
이 말은, 여러 종류의 컨테이너가 동일한 시스템에서 즉 내 피씨에서 실행되고 OS커널을 다른 컨테이너와 공유할 수 있고, 각 컨테이너는 사용자 공간에서 분리된 프로세스로 실행되는 것입니다

도커는 vm보다 메모리 공간을 적게 차지하고 더 많은 어플리케이션을 처리할 수 있으며 더 적은 수의 vm 또는 os를 필요로 합니다!

쉽게 풀면 하나의 HostOS위에 도커를 설치해 그 위에 각각의 어플리케이션 환경들을 설치하며 운영하는 형태입니다!
각각 OS에 설치된것이 아닌 하나의 호스트OS위에서 자원만 공유하기에 상대적으로 가벼우며 도커가 설치된 환경이라면 이미지가 사용 가능하기에 어디서든 사용이 가능하다는 장점을 가지고 있습니다

Vm은
하나의 서버를 여러 서버로 전화하는 물리적인 하드웨어의 추상화라고 정의할 수 있고
하이퍼바이저 기법을 통해 단일 시스템에서 여러 VM을 실행할 수 있지만, 각 VM엔 OS, 어플리케이션, 필요한 바이너리 및 라이브러리의 전체 복사본이 포함되어 수십 GB를 차지하기에 VM의 부팅 속도 또한 느려질수도 있습니다

즉 VM가상머신은 하이퍼바이저를 이용해 하나의 호스트OS에서 여러 개의 OS를 사용하는 방법이며,
VM구조와 같은 기반인 호스트OS 위에 각각의 게스트OS를 하나씩 설치하는 형태입니다
이는 각각의 가상머신은 하나의 독립된 커널 공간을 가진 완전한 컴퓨터를 생산하는 식의 환경을 구성하게 됩니다

도커와 달리 용량이 매우 무겁습니다 하지만 다른 게스트OS와 분리 독립된 공간과 자원을 할당받아 사용하기에 보안성 측면에서 효율적입니다!

`13번` - CI/CD가 무엇이라고 생각하시나요? CI와 CD의 차이점이 무엇인지 설명해 주세요.

`14번` - 본인이 구현해 본 CI/CD 배포 자동화 과정을 설명해 주세요.
