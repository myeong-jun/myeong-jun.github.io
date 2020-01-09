# 2019-12-30-HTTP,Web,Docker
## **HTTP**
 
* HTML(Hypertext Markup Language) 문서를 교환하기 위해 만들어진 통신교약, 다른 컴퓨터가 서로 텍스트를 주고 받을때 서로 이해할 수 있는 정해진 '규격' 으로 보내져야하는데 HTTP가 바로 그 메세지를 보내기에 맞춰진 프로토콜(복수의 컴퓨터 사이나 단말기 사이에서 데이터 통신을 원활하게 하기 위해 필요한 통신규약)이다.
 
![HTTP](https://mdn.mozillademos.org/files/13677/Fetching_a_page.png)
 
### **통신방식**
 
* HTTP는 기본적으로 요청/응답(request/response) 구조이다.
    + 클라이언트가 HTTP request를 서버에 보내면 서버는 HTTP response를 보내는 구조
    + 클라이언트와 서버의 모든 통신이 요청과 응답으로 이루어짐
* HTTP는 stateless
    + state(상태)를 저장하지 않는다.
    + 요청이 오면 그에 응답을 하고 여러 요청/응답끼리 연결되어 있지 않다.
    + 여러 요청과 응답의 데이터가 필요할때는 쿠키나 세션을 사용한다.
 
### **HTTP request, reponse 구조**
 
* HTTP request 크게 3가지로 구성
    + start line
        - HTTP request의 첫 라인이며 3부분으로 구성
            1. HTTP Method : 해당 request가 의도한 action을 정의 하는 부분
            2. REquest target : request가 전송되는 목표 url (예: /login)
            3. HTTP version
    + headers
        - 해당 request에 대한 추가정보를 담고 있는 부분이다.
        - Key:Value 값으로 되어있고 크게 3부분으로 구성되어있다.
        - 자주 사용하는 header 정보
            1. Host : 요청이 전송되는 target의 host url -> google.com
            2. User-Agent : 요청을 보내는 클라이언트에 대한 정보
            3. Accept : 해당 요청이 받을 수 있는 응답 타임.
            4. Connection : 해당 요청이 끝난 후 클라이언트와 서버가 계속해서 네트워크 컨넥션을 유지할지 지시하는 부분.
            5. Content-Type : 해당 요청이 보내는 메시지 body의 타입
            6. Content-Length : 메시지 body의 길이       
    + body
        - 해당 request의 실제 메시지 내용이며 Body가 없는 요청도 많다.
* HTTP Response 크게 3부분으로 구성
    + Status line
        - Response의 상태를 나타내주는 부분
        - 예) HTTP/1.1 404 Not Found
    + Headers
        - Response의 headers와 동일하다 다만 값들은 차이가 있다.
    + Body
        - Response의 body와 동일하며 모든 response에 body가 있지는 않다.
        
 
----
 
## **Web**

![web](https://www.pinno.kr/resources/img/sub/b_w_06.png)

* web이란 인터넷에 연결된 사용자들이 서로의 정보를 공유할 수 있는 공간을 의미합니다. 간단히 줄여서 www나 w3라고도 부르며, 간단히 웹(web)이라고 불린다. 

### **Web의 특징**

* web은 인터넷 상에서 텍스트나 그림, 소리, 영상 등과 같은 멀티미디어 정보를 하이퍼텍스트 방식으로 연결하여 제공합니다. 하이퍼텍스트란 문서 내부에 또 다른 문서로 연결되는 참조를 집어 넣음으로써 웹 상에 존재하는 여러 문서끼리 서로 참조할 수 있는 기술을 의마한다. 이 때 문서 내부에서 또 다른 문서로 연결되는 참조를 하이퍼링크(hyperlink)라고 부른다. 웹에서는 HTML이라는 언어를 사용하여 누구나 자신만의 문서를 작성할 수 있다. 또한, 이렇게 만든 문서에를 HTTP라는 프로토콜을 사용하면 누구나 검색하고 접근 할 수 있다.

### **Web의 구성**

* Web에서 크게 다섯가지로 분류 될수 있다.
    + 웹 페이지(Web page)
        - HTML 언어를 사용하여 작성된 하이퍼텍스트 문서
    + 웹 사이트(Web site)
        - 웹 페이지들 중에서 서로 관련된 내용으로 작성된 웹 페이지들의 집합
    + 하이퍼링크(hyperlink)
        - 웹은 수 많은 웹 페이지들이 하이퍼링크를 통해 서로 연결되어 구성
    + 웹 서핑(web surfing)
        - 사용자가 웹 페이지에 포함된 하이퍼링크를 따라 따른 웹 페이지들로 계속하여 이동하는 것
    + 웹 브라우저(web browser)
        - 사용자가 웹 페이지를 검색하기 위해 사용하는 프로그램

---

## **Docker**
 
![Docker](https://subicura.com/assets/article_images/2017-01-19-docker-guide-for-beginners-1/docker-works.png)
 
* 도커는 애플리케이션을 신속하게 구축, 테스트 및 배포할 수 있는 컨테이너 기반의 오픈소스 가상화 플랫폼입니다.
서버에서 이야기하는 컨테이너는 다양한 프로그램, 실행환경을 컨테이너로 추상화하고 동일한 인터페이스를 제공하여 프로그램의 배포 및 관리를 단순하게 해줍니다. 
백엔드 프로그램, 데이터베이스 서버, 메시지 큐등 어떤 프로그램도 컨테이너로 추상화 할 수 있다.
 
### **컨테이너**
 
![컨테이너](https://subicura.com/assets/article_images/2017-01-19-docker-guide-for-beginners-1/docker-container.png)
 
* 컨테이너는 격리된 공간에서 프로세스가 동작하는 기술이다. 기존의 OS를 가상화 방식과는 다르게 CPU의 가상화 기술을 이용한 KVM과 반가상화 방신의 Xen을 이용한다. CPU나 메모리는 프로세스가
필요한 만큼만 추가로 사용하고 성능적으로도 손실이 거의 없다.
하나의 서버에 여러개의 컨테이너를 실행하면 서로 영향을 미치지 않고 독립적으로 실행된다. 
 
### **이미지**
 
![이미지](https://subicura.com/assets/article_images/2017-01-19-docker-guide-for-beginners-1/docker-image.png)
 
* 컨테이너 실행에 필요한 파일과 설정값등을 포함하고 있는 것으로 상태값을 가지지않고 변하지 않는다.
컨테이너는 이미지를 실행한 상태라고 볼 수 있고 추가되거나 변하는 값은 컨테이너에 저장된다.
같은 이미지에서 여러개의 컨테이너를 생성할 수 있고 컨테이너의 상태가 바뀌거나 컨테이너가 삭제되더라도 이미지는 변하지 않고 그대로 남아있다.

