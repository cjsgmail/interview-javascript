# 기술면접준비

## javascript

> ### 자바스크립트의 특징

* 객체기반의 스크립트 언어입니다.
* 자바스크립트는 동적 타이핑 언어입니다. 
  * 동적 언어는 소스 실행 시 타입이 결정되기 때문에 변수에 예상치 못한 타입이 들어와 Type Error가 발생하는 경우가 생길 수 있습니다. 이것은 TypeScript를 사용하는 이유이기도 합니다.
* 싱글 스레드 언어입니다. 따라서 동기적으로 동작합니다.

> ### 타입스크립트의 특징

* 타입스크립트는 자바스크립트를 기반으로 정적 타입 문법을 추가한 프로그래밍 언어입니다.
* 자바스크립트는 동적 타입의 인터프리터 언어로 런타임에서 오류를 발견할 수 있습니다. 
* 이에 반해 타입스크립트는 정적 타입의 컴파일 언어이며 타입스크립트 컴파일러 또는 바벨(Babel)을 통해 자바스크립트 코드로 변환됩니다. 
* 코드 작성 단계에서 타입을 체크해 오류를 확인할 수 있고 미리 타입을 결정하기 때문에 실행 속도가 매우 빠르다는 장점이 있습니다. 
* 하지만, 새로운 프로그래밍 언어에 대한 러닝 커브(Learning Curve), 상대적으로 낮은 가독성, 코드량 증가 등의 단점이 있습니다.

> ### 그렇다면 JS가 좋은가요 TS가 좋은가요?

* 프로젝트 성격에 따라 타입스크립트를 사용할지 결정하면 됩니다. 
* 프로젝트의 규모가 크고 복잡할수록, 유지보수가 중요한 장기 프로젝트일수록 타입스크립트의 이점이 부각될 것입니다.

> ### 스코프란?

* 식별자(변수)에 접근할 수 있는 범위
* 전역 스코프와 지역 스코프로 나눌수 있다.
* 전역 스코프: 어느 곳에서나 접근이 가능한 범위.
* 지역 스코프: 해당 지역에서만 접근이 가능한 범위.
  * 함수 스코프: 함수에서 선언한 변수는 해당 함수 내에서만 접근 가능한 것을 의미
  * 블록 스코프: 블록({}) 내부에서 선언된 변수는 해당 블록에서만 접근 가능한 것을 의미
  * lexical 스코프: 변수, 함수가 선언된 곳에 따라 정의되는 스코프 (js)
  * dynamic 스코프: 변수, 함수가 호출된 곳에 따라 정의되는 스코프

> ### 호이스팅이란?

* JavaScript에서 호이스팅(hoisting)이란, 인터프리터가 변수와 함수의 메모리 공간을 선언 전에 미리 할당하는 것을 의미합니다.
* `var`로 선언한 변수의 경우 호이스팅 시 `undefined`로 변수를 초기화합니다. 반면 `let`과 `const`로 선언한 변수의 경우 호이스팅 시 변수를 초기화하지 않습니다.

> ### 클로저 함수란?

* 함수와 함수가 선언된 어휘적 환경의 조합, 외부함수의 변수에 접근 가능한 내부함수
* 사용하는 이유: 상태가 의도치 않게 변경되지 않도록 안전하게 은닉하고 특정 함수에게만 상태 변경을 허용하여 상태를 안전하게 변경하고 유지하기 위해 사용합니다.

* 모듈패턴 : 모듈 패턴은 JavaScript 에서 중요한 패턴 중 하나이며 가장 일반적으로 사용되는 디자인 패턴이다. 프로젝트의 코드 단위를 명확하게 분리하고 구성하는데 큰 도움이 된다. 클래스를 모방해서 관련이 있는 변수와 함수를 모아 즉시실행함수()로 감싸서 하나의 모듈을 만들어 클로저를 기반으로 동작합니다.
  * 캡슐화 : 정보은닉을 구현하기 위해서 모듈패턴을 사용합니다.
  * 전역변수의 억제
  * 재사용성

> ### 자료형

* 원시자료형
  * 할당시 메모리에 고정된 크기로 저장되고, 변수에 값이 담김
  * 선언, 초기화, 할당 시 값이 저장된 메모리에 직접 접근
  * number, string, boolean, undefined
* 참조자료형
  * 데이터 크기가 정해지지 않고, 변수에는 값이 저장된 주소가 담김
  * array, object, function

> ### 정적타입, 동적타입의 차이

* 정적타입
  * 타입을 컴파일 시에 결정, 변수의 타입지정 필요
  * C, C#, C++, Java
* 동적타입
  * 타입지정없이 변수에 값 할당
  * 런타임때 값의 타입에 따라 자동 결정
  * JavaScript, Ruby, Python, SmallTalk
  
> ### ==(동치연산자), ===(일치연산자) 차이점

* 동치연산자
  * 강제 형 변환 (비교전 두 피연산자를 공통 타입으로 바꾸고 값 비교)
* 일치연산자
  * 값과 데이터타입 비교

> ### event loop란?

* 브라우저는 특정 이벤트가 발생하면 이를 감지해 미리 정해둔 작업을 수행한다.여러 이벤트가 동시 발생할경우, 이벤트루프가 실행 순서를 정해준다.
* event loop는 콜스택에 처리중인 태스크가 없는지, 태스크 큐에 대기중인 태스크가 있는지 반복 확인한다.
* 콜스택이 비고, 태스크 큐에 대기중인 함수가 있으면 콜스택으로 이동시킨다.

> ### DOM에 대하여 설명

* DOM 은 nodes와 objects로 문서를 표현한다.
* DOM 은 문서를 표현하고, 저장하고, 조작하는 방법을 제공한다. DOM 은 웹 페이지의 객체 지향 표현이며, 자바스크립트와 같은 스크립팅 언어를 이용해 DOM 을 수정할 수 있다.

> ### DOM과 Virtual DOM의 차이

* DOM은 Document Object Model로 HTML 코드로 설계된 웹페이지가 브라우저 안에서 화면에 나타나고, 이벤트에 반응하며, 값을 입력받는 등 기능들을 수행할 객체들로 실체화된 형태를 의미합니다.
* Virtual DOM은 실제 DOM을 모방하는 형태로 메모리 상에서만 존재하는 가상의 DOM을 의미합니다. 
* 변화가 실제 DOM에 적용되기 전 가상의 DOM을 한번 거쳐 미리 처리하고 저장한 후 실제 DOM에 업데이트 할 수 있게 해줍니다.
* 최근에는 Single Page Application을 많이 사용하면서 DOM tree를 즉각적으로 변경할 일이 생겼습니다. 
* 전체 페이지를 서버에서 매번 보내주는 것이 아니라, 브라우저 단에서 자바스크립트가 관리하기 때문에, DOM조작을 더욱 더 효율적으로 할 수 있게 최적화가 필요하게 되었고 그래서 가상 돔이 등장하게 되었습니다.

> ### 그렇다면 가상 DOM이 항상 효율적인가요?

* 사용자와 상호작용이 많은 웹에서는 더 효율적이지만 단순 정보제공만 하는 웹에선 일반 Dom이 더 효율적일 수 있습니다.


> ### API란?

* 요청과 응답을 사용하여 두 애플리케이션이 서로 통신하는 방법을 정의
* API 아키텍처는 일반적으로 클라이언트와 서버 측면에서 설명된다. 요청을 보내는 애플리케이션을 클라이언트라고 하고 응답을 보내는 애플리케이션을 서버라고 한다.

> ### REST API란?
* REST API는 웹에서 사용되는 데이터나 자원(Resource)을 HTTP URI로 표현하고, HTTP 프로토콜을 통해 요청과 응답을 정의하는 방식을 말한다.
* 알아보기 쉽고 잘 작성된 메뉴판이 필요, 이 역할을 API가 수행해야 하므로 모두가 잘 알아볼 수 있도록 작성

> ### REST 성숙도 모델 4단계 (0~3단계)

* REST 성숙도 모델 - 0단계
  * 단순히 HTTP 프로토콜을 사용하기만 해도 된다.
  * 물론 이경우 해당 API를 REST API라고 할 수 없다.
  * 0단계는 REST API를 작성하기 위한 기본 단계
  
* REST 성숙도 모델 - 1단계
  * 1단계에서는 개별 리소스와의 통신을 준수
  * 웹에서 사용되는 모든 데이터나 자원을 HTTP URI로 표현한다.
  * 개별 리소스에 맞는 엔드포인트를 사용해야한다.
  * 요청하고 받는 자원에 대한 정보를 응답으로 전달해야 한다.

* REST 성숙도 모델 - 2단계
  * CRUD에 맞게 적절한 HTTP 메서드를 사용하는 것에 중점을 둔다.
  * GET 메서드는 body를 가지지 않기 때문에 query parameter를 사용하여 리소스를 전달
  * POST요청에 대한 응답은 새롭게 생성된 리소스를 보내주기 때문에,
  * 응답 코드는 201 Created 로 명확하게 작성한다.
  * 관련 리소스 클라이언트가 Location 헤더에 작성된 URI를 통해 확인할 수 있도록 하면
  * 완벽하게 REST 성숙도 모델의 2단계를 충족한 것

* REST 성숙도 모델 - 3단계
  * HATEOAS(Hypertext As The Engine Of Application State)라는 약어로 표현되는 하이퍼미디어 컨트롤을 적용한다.
  * 3단계의 요청은 2단계와 동일
  * 응답에는 리소스의 URI를 포함한 링크 요소를 삽입하여 작성한다.
  * 응답 내에 새로운 링크를 넣어 새로운 기능에 접근할 수 있도록 하는 것이 3단계의 핵심
  * 실제로 엄밀하게 3단계까지 지키기 어렵기 때문에 2단계까지만 적용해도 좋은 API 디자인이라고 볼 수 있고, 이런 경우를 HTTP API 라고도 부른다.
  
> ### 전역상태관리를 사용하는 이유

* 전역 상태관리를 사용하지 않으면 상태 끌어올리기, Props 내려주기를 여러 번 거쳐야 합니다. 
* 따라서 해당 상태를 직접 사용하지 않는 컴포넌트들도 상태 데이터를 가지기 때문에 애플리케이션이 복잡해질수록 데이터 흐름도 복잡해집니다.
* 그리고 컴포넌트 구조가 바뀐다면, 지금의 데이터 흐름을 완전히 바꿔야 할 수도 있습니다.
  
## 리액트

> ### 리액트의 생명주기

* 라이프 사이클이란 컴포넌트의 마운트, 업데이트, 언마운트 과정을 의미합니다.
* 함수형 리액트에서는 useEffect를 통해 컴포넌트의 마운트, 업데이트, 언마운트를 관리할 수 있습니다. 
* useEffect는 컴포넌트 안에서 state와 props에 접근이 가능하고 기본적으로 첫 번째 렌더링과 그 이후의 모든 업데이트에서 사용됩니다. 
* 그리고 모든 effect는 정리를 위한 클린업 함수를 반환할 수 있는데 이는 컴포넌트가 언마운트될 때 실행됩니다.

> ### 리액트는 왜 스테이트를 setState를 사용해서 변경시키는가

* 직접 값을 바꾸게 되면 리렌더링이 되지않고 setState를 통해서 바꾸는 것만 리렌더링이 되기 때문에 setState를 사용해서 state를 변경해야 합니다.

## 퍼블리싱

> ### UX와 UI

* UX란?
  * User Experience, 사용자 경험
  * 사용자가 어떤 시스템, 제품, 서비스를 직/간접적으로 이용하면서 느끼고 생각하는 총체적 경험
  * 경험은 물론, 홍보, 접근성, 사후 처리 등 직간접적으로 관련된 모든 경험을 사용자 경험이라고 한다.
  
* UI란?
  * User Interface, 사용자 인터페이스
  * 사람들이 컴퓨터와 상호 작용하는 시스템을 의미
  * 화면상의 그래픽 요소 외에도 키보드, 마우스 등의 물리적 요소도 컴퓨터와 상호 작용하기 위한 시스템이므로 UI
  * 화면과의 상호 작용을 통해 사용하는 기기들을 어렵지 않게 찾아볼 수 있다. 이처럼 현대 사회에서는 그래픽 UI, 즉, GUI(Graphical User Interface)가 굉장히 중요한 역할을 하게 되었다.
  
<p>UX는 UI를 포함하지만 좋은 UX가 좋은 UI를 의미하거나, 좋은 UI가 항상 좋은 UX를 보장하지는 않는다. 
세련되고 보기 좋은 UI의 계산기가 있다고 생각해 보자. 그런데 입력한 숫자가 아닌 다른 숫자가 화면에 뜨거나, 계산 결과값이 제대로 나오지 않는다면 어떨까? UI가 아무리 보기 좋아도 UX는 좋지 않을 것이다.
하지만, 나쁜 UI는 보통 나쁜 UX를 유발한다.<p>

> ### CSS position에 대하여

* position absolute
  * 요소를 일반적인 문서 흐름에서 배제하며 가장 가까운 위치에 있는 부모(조상)요소를 기준으로 배치된다.
  * 부모 요소를 기준으로 상[top], 하[bottom], 좌[left], 우[right] 로 얼마나 간격을 두고 배치할 것인지 결정한다.
  * 부모 positon이 없이 단독으로 사용될 경우 <body>를 기준
  
* position relative
  * 현위치를 기준으로 상[top], 하[bottom], 좌[left], 우[right] 로 얼마나 간격을 두고 배치할 것인지 결정한다.
  * 위치 이동을 하면서 다른 요소에 영향을 끼치지 않으며 문서상으로 원위치 그대로 유지가 가능하다.
  
## Git

> ### Git merge 와 Git rebase

* merge를 이용해서 병합하는 방식은 하나의 merge commit이 생성되면서 합쳐집니다. 
* rebase는 rebase가 되는 베이스 브랜치에 합쳐질 브랜치들의 커밋이 새로운 커밋으로 각각 줄줄이 생기면서 합쳐집니다. 
* 따라서 rebase 방식은 각 커밋마다 충돌이 일어날 수 있지만 변경이력을 알기 쉽기 때문에 히스토리 관리가 용이합니다. 
* 반면에 merge는 단순히 브랜치를 합치는 것이기 때문에 병합이 쉽지만 프로젝트가 활발한 경우 매번 생기는 merge 커밋 때문에 변경이력을 알기 어렵습니다. 

## CS

> OSI 7계층

1 계층인 물리 계층에서 데이터를 전기 신호로 바꾸어줍니다.
2 계층인 데이터링크 계층에서 데이터의 물리적인 전송과 에러 검출, 흐름 제어를 담당합니다.
3 계층인 네트워크 계층에서 패킷을 목적지까지 가장 빠른 길로 전송합니다.
4 계층인 전송 계층에서 최종 수신 프로세스로 데이터를 전송합니다.
5 계층인 세션 계층에서 컴퓨터끼리 통신을 하기 위해 세션을 만듭니다.
6 계층인 표현 계층에서 데이터의 형식을 정의합니다.
마지막으로 7 계층인 응용 계층은 사용자와 직접 상호작용하는 응용 프로그램들이 포함합니다.









  
