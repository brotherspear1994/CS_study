# OSI 7계층

![img](https://media.vlpt.us/images/dyllis/post/7a6679e2-26e0-4d3e-b792-c866b9012226/%EB%8B%A4%EC%9A%B4%EB%A1%9C%EB%93%9C.png)

### OSI 7 계층이란?

OSI 7 계층은 네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것을 말한다. 

### OSI 7 계층을 나눈이유는?



계층을 나눈 이유는 통신이 일어나는 과정이 단계별로 파악할 수 있기 때문이다.



흐름을 한눈에 알아보기 쉽고, 사람들이 이해하기 쉽고,

7단계 중 특정한 곳에 이상이 생기면 다른 단계의 장비 및 소프트웨어를 건들이지 않고도 이상이 생긴 단계만 고칠 수 있기 때문이다.

(It is because of the fact that it will be **easy for troubleshooting the network problems**. 

Only the layer in which the problem exist will be modified. Other layers are left untouched.)



그럼 문제를 예로 들어보자



 PC방에서 오버워치를 하는데 연결이 끊겼다.  어디에 문제가 있는지 확인하기 위해서는  모든 PC가 문제가 있다면 라우터의 문제(3계층 네트워크 계층)이거나 광랜을 제공하는 회사의 회선 문제(1계층 물리 계층)  한 PC만 문제가 있고  오버워치 소프트웨어에 문제가 있다면(7계층 어플리케이션 계층) 오버워치 소프트웨어에 문제가 없고, 스위치에 문제가 있으면(2계층 데이터링크 계층) 있다고 판단해 다른 계층에 있는 장비나 소프트웨어를 건들이지 않는것이다.



## 계층 기능

### 계층 1: 물리 계층

![<nowiki ></nowiki>](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Crystal_Clear_app_xmag.svg/16px-Crystal_Clear_app_xmag.svg.png)이 부분의 본문은 [물리 계층](https://ko.wikipedia.org/wiki/물리_계층)입니다.

물리 계층(Physical layer)은 네트워크의 기본 네트워크 하드웨어 전송 기술을 이룬다. 네트워크의 높은 수준의 기능의 논리 데이터 구조를 기초로 하는 필수 계층이다. 다양한 특징의 하드웨어 기술이 접목되어 있기에 OSI 아키텍처에서 가장 복잡한 계층으로 간주된다.

- 데이터를 전기 수신호(0과 1 비트)로 변환 및 전송. 

- 7계층 중 최하위 계층입니다. 주로 전기적, 기계적, 기능적인 특성을 이용해 데이터를 전송하게 됩니다. 데이터는 0과 1의 비트열, 즉 On, Off의 전기적 신호 상태로 이루어져있지요.

  이 계층은 단지 데이터를 전달하기만 합니다. 어떤 에러가 있는지 등 그런 기능에는 전혀 관여하지 않습니다.

### 계층 2: 데이터 링크 계층

![<nowiki ></nowiki>](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Crystal_Clear_app_xmag.svg/16px-Crystal_Clear_app_xmag.svg.png)이 부분의 본문은 [데이터 링크 계층](https://ko.wikipedia.org/wiki/데이터_링크_계층)입니다.

데이터 링크 계층(Data[[3\]](https://ko.wikipedia.org/wiki/OSI_모형#cite_note-3)link layer)은 포인트 투 포인트(Point to Point) 간 신뢰성있는 전송을 보장하기 위한 계층으로 CRC 기반의 오류 제어와 흐름 제어가 필요하다. 네트워크 위의 개체들 간 [데이터](https://ko.wikipedia.org/wiki/데이터)를 전달하고, 물리 계층에서 발생할 수 있는 오류를 찾아 내고, 수정하는 데 필요한 기능적, 절차적 수단을 제공한다. 주소 값은 물리적으로 할당 받는데, 이는 네트워크 카드가 만들어질 때부터 맥 주소(MAC address)가 정해져 있다는 뜻이다. 주소 체계는 계층이 없는 단일 구조이다. 데이터 링크 계층의 가장 잘 알려진 예는 [이더넷](https://ko.wikipedia.org/wiki/이더넷)이다. 이 외에도 HDLC나 ADCCP 같은 포인트 투 포인트(point-to-point) 프로토콜이나 패킷 스위칭 네트워크나 LLC, [ALOHA](https://ko.wikipedia.org/wiki/알로하_프로토콜) 같은 근거리 네트워크용 프로토콜이 있다. 네트워크 브릿지나 스위치 등이 이 계층에서 동작하며, 직접 이어진 곳에만 연결할 수 있다.

- 프레임에 주소부여(MAC - 물리적주소)

- 에러검출/재전송/흐름제어

- 물리 계층에서 송수신되는 정보의 오류와 흐름을 관리하여 안전한 정보의 전달을 수행할 수 있도록 도와주는 역할을 합니다.

  데이터 링크 계층의 데이터 전송은 Point-To-Point 간 입니다. 

  안전한 정보의 전달이라는 것은 오류나 재전송하는 기능을 갖고 있다는 이야기죠. 또한 우리가 언젠가 한번 들었을 MAC주소를 갖고 있습니다. 그래서 통신을 할 수 있지요.

  - MAC 주소: **MAC 주소**(Media Access Control **Address**)는 네트워크 세그먼트의 데이터 링크 계층에서 통신을 위한 네트워크 인터페이스에 할당된 고유 식별자이다.

  

  이 계층에서 부르는 데이터의 단위는 프레임(Frame)이라고 합니다.

### 계층 3: 네트워크 계층

![<nowiki ></nowiki>](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Crystal_Clear_app_xmag.svg/16px-Crystal_Clear_app_xmag.svg.png)이 부분의 본문은 [네트워크 계층](https://ko.wikipedia.org/wiki/네트워크_계층)입니다.

네트워크 계층(Network layer)은 여러개의 노드를 거칠때마다 경로를 찾아주는 역할을 하는 계층으로 다양한 길이의 [데이터](https://ko.wikipedia.org/wiki/데이터)를 네트워크들을 통해 전달하고, 그 과정에서 전송 계층이 요구하는 [서비스 품질](https://ko.wikipedia.org/wiki/서비스_품질)(QoS)을 제공하기 위한 기능적, 절차적 수단을 제공한다. 네트워크 계층은 라우팅, 흐름 제어, 세그멘테이션(segmentation/desegmentation), 오류 제어, 인터네트워킹(Internetworking) 등을 수행한다. 라우터가 이 계층에서 동작하고 이 계층에서 동작하는 스위치도 있다. 데이터를 연결하는 다른 네트워크를 통해 전달함으로써 인터넷이 가능하게 만드는 계층이다. 논리적인 주소 구조(IP), 곧 네트워크 관리자가 직접 주소를 할당하는 구조를 가지며, 계층적(hierarchical)이다.

서브네트의 최상위 계층으로 경로를 설정하고, 청구 정보를 관리한다. 개방형 시스템들의 사이에서 네트워크 연결을 설정, 유지, 해제하는 기능을 부여하고, 전송 계층 사이에 네트워크 서비스 데이터 유닛(NSDU : Network Service Data Unit)을 교환하는 기능을 제공한다.

- 주소부여(IP)

- 경로설정(Route)

- 네트워크 계층은 네트워크에서 아주 중요합니다.

  중요한 기능 중 한가지는 바로 라우팅이라고 하는데요. 목적지까지 가장 안전하고 빠르게 데이터를 보내는 기능을 말합니다. 따라서 최적의 경로를 설정해야하지요.

  이런 라우팅 기능을 맡고 있는 계층이 네트워크 계층입니다.

  

  또한 어느 컴퓨터에게 데이터를 전송할지 주소를 갖고 있어서 통신을 합니다. 우리가 자주 듣는 IP 주소가 바로 네트워크 계층 헤더에 속해있습니다.

  

  네트워크 계층에서 부르는 데이터 단위는 패킷(Packet)이라고 합니다.

### 계층 4: 전송 계층

![<nowiki ></nowiki>](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Crystal_Clear_app_xmag.svg/16px-Crystal_Clear_app_xmag.svg.png)이 부분의 본문은 [전송 계층](https://ko.wikipedia.org/wiki/전송_계층)입니다.

전송 계층(Transport layer)은 양 끝단(End to end)의 사용자들이 신뢰성있는 [데이터](https://ko.wikipedia.org/wiki/데이터)를 주고 받을 수 있도록 해 주어, 상위 계층들이 데이터 전달의 유효성이나 효율성을 생각하지 않도록 해준다. 시퀀스 넘버 기반의 오류 제어 방식을 사용한다. 전송 계층은 특정 연결의 유효성을 제어하고, 일부 프로토콜은 상태 개념이 있고(stateful), 연결 기반(connection oriented)이다. 이는 전송 계층이 패킷들의 전송이 유효한지 확인하고 전송 실패한 패킷들을 다시 전송한다는 것을 뜻한다. 가장 잘 알려진 전송 계층의 예는 [TCP](https://ko.wikipedia.org/wiki/전송_제어_프로토콜)이다.

종단간(end-to-end) 통신을 다루는 최하위 계층으로 종단간 신뢰성 있고 효율적인 데이터를 전송하며, 기능은 오류검출 및 복구와 흐름제어, 중복검사 등을 수행한다.

- 패킷 생성(Assembly/Sequencing/Deassembly/Error detection/Request repeat/Flow control)

- 전송 계층 역시 네트워크에서 중요한 계층입니다. 전송 계층은 양 끝단의 사용자들이 신뢰성있는 데이터를 주고 받게 해주는 역할을 합니다.

  송신자와 수신자 간의 신뢰성있고 효율적인 데이터를 전송하기 위하여 오류검출 및 복구, 흐름제어와 중복검사 등을 수행합니다.

  

  중요한 것은 데이터 전송을 위해서 Port 번호가 사용이 됩니다. 대표적인 프로토콜로는 TCP와 UDP가 있습니다. 이 계층에서 사용하는 데이터 단위는 세그먼트(Segment)라고 합니다.

### 계층 5: 세션 계층

![<nowiki ></nowiki>](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Crystal_Clear_app_xmag.svg/16px-Crystal_Clear_app_xmag.svg.png)이 부분의 본문은 [세션 계층](https://ko.wikipedia.org/wiki/세션_계층)입니다.

세션 계층(Session layer)은 양 끝단의 응용 프로세스가 통신을 관리하기 위한 방법을 제공한다. 동시 송수신 방식(duplex), 반이중 방식(half-duplex), 전이중 방식(Full Duplex)의 통신과 함께, 체크 포인팅과 유휴, 종료, 다시 시작 과정 등을 수행한다. 이 계층은 TCP/IP 세션을 만들고 없애는 책임을 진다.

통신하는 사용자들을 동기화하고 오류복구 명령들을 일괄적으로 다룬다.

- 통신을 하기 위한 세션을 확립/유지/중단 (운영체제가 해줌)
- 두 네트워트간의 연결 유지, 세션을 만들고 없애는 역할.

### 계층 6: 표현 계층

![<nowiki ></nowiki>](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Crystal_Clear_app_xmag.svg/16px-Crystal_Clear_app_xmag.svg.png)이 부분의 본문은 [표현 계층](https://ko.wikipedia.org/wiki/표현_계층)입니다.

표현 계층(Presentation layer)은 코드 간의 번역을 담당하여 사용자 시스템에서 [데이터](https://ko.wikipedia.org/wiki/데이터)의 형식상 차이를 다루는 부담을 응용 계층으로부터 덜어 준다. [MIME](https://ko.wikipedia.org/wiki/MIME) 인코딩이나 암호화 등의 동작이 이 계층에서 이루어진다. 예를 들면, [EBCDIC](https://ko.wikipedia.org/wiki/EBCDIC)로 인코딩된 문서 [파일](https://ko.wikipedia.org/wiki/컴퓨터_파일)을 [ASCII](https://ko.wikipedia.org/wiki/ASCII)로 인코딩된 파일로 바꿔 주는 것이 표현 계층의 몫이다.

- 사용자의 명령어를 완성및 결과 표현.

- 포장/압축/암호화

- 데이터를 어떻게 표현할 지 정하는 역할을 하는 계층으로 일종의 확장자라고 이야기하면 편하겠네요.

  표현 계층은 세가지의 기능을 갖고 있습니다.

  

  \1. 송신자에서 온 데이터를 해석하기 위한 응용계층 데이터 부호화, 변화

  \2. 수신자에서 데이터의 압축을 풀수 있는 방식으로 된 데이터 압축

  \3. 데이터의 암호화와 복호화

  

  MIME 인코딩이나 암호화 등의 동작이 표현계층에서 이루어집니다. EBCDIC로 인코딩된 파일을 ASCII 로 인코딩된 파일로 바꿔주는 것이 한가지 예이지요.

### 계층 7: 응용 계층

![<nowiki ></nowiki>](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Crystal_Clear_app_xmag.svg/16px-Crystal_Clear_app_xmag.svg.png)이 부분의 본문은 [응용 계층](https://ko.wikipedia.org/wiki/응용_계층)입니다.

응용 계층(Application layer)은 응용 프로세스와 직접 관계하여 일반적인 응용 서비스를 수행한다. 일반적인 응용 서비스는 관련된 응용 프로세스들 사이의 전환을 제공한다. 응용 서비스의 예로, 가상 터미널(예를 들어, [텔넷](https://ko.wikipedia.org/wiki/텔넷)), "Job transfer and Manipulation protocol" (JTM, 표준 ISO/IEC 8832) 등이 있다.

- 네트워크 소프트웨어 UI 부분
- 사용자의 입출력(I/O)부분

