# 202330137 백채원

## java2-1
개요는 리드미에 나온다

## 3월 15일 강의
내용정리

## 3월 22일 강의
자바의 특성
1. 플랫폼 독립성
하드웨어, 운영체제에 종속되지 않는 바이트 코드로 플랫폼 독립성
2. 객체지향
캡슐화, 상속, 다형성 지원
3. 클래스로 캡슐화
자바의 모든 변수나 함수는 클래스 내에 선언, 클래스 안에서 클래스(내부 클래스 작성 가능)

소스(.java)와 클래스(.class)파일
1. 하나의 소스 파일에 여러 클래스 작성 가능(public 클래스는 하나만 가능)
2. 소스 파일의 이름과 public으로 선언도니 클래스 이름은 같아야 함
3. 클래스 파일에는 하나의 클래스만 존재(다수의 클래스를 가진 자바 소스를 컴파일하면 클래스마다 별도 클래스 파일 생성)

자바의 특징(2)
  실행코드 배포
구성
- 한 개의 class 파일 또는 다수의 파일로 구성
- 여러 폴더에 걸쳐 다수의 클래스 파일로 구성된 경우:jar 압축 파일로 배포
자바 응용프로그램의 실행은 main() 메소드에서 시작
- 하나의 클래스 파일에 두 개 이상의 main() 메소드가 있을 수 없음

자바의 특징(3)
실시간 응용 프로그램에 부적합
- 실행 도중 예측할 수 없는 기점에 가비지 컬렉션 실행 때문
자바 프로그램은 안전
- 타임 체크 엄격
물리적 주소를 사용하는 포인터 개념 없음
프로그램 작성 쉬움
- 포인터 개념이 없음
- 물리적 주소를 사용하는 포인터 개념 없음
프로그램 작성 쉬움
- 포인터 개념이 없음
- 동적 메모리 반환 하지 않음
- 다양한 라이브러리 지원
실행 속도 개선을 위한 JIT 컴파일러 사용
- 자바는 바이트 코드를 인터프리터 방식으로 실행(기계어가 실행되는 것보다 느림)
- JIT 컴파일 기법으로 실행 속도 개선(JIT 컴파일-실행 중에 바이트 코드를  기계어 코드로 컴파일하여 기계어를 실행하는 기법)


## 3월 29일 강의
자바의 키 입력과 System.in

System.in
- 키보드와 연결된 자바의 표준 입력 스트림
- 입력되는 키를 바이트(문자 아님)로 리턴하는 저수준 스트림
- System.in을 직접 사용하면 바이트를 문자나 숫자로 변환하는 많은 어려움 있음

Scanner를 이용한 키 입력
Scanner는 입력되는 키 값을 공백으로 구분되는 토큰 단위로 읽음
- 개발자가 원하는 타입 값으로 쉽게 읽을 수 있음

반복문
자바 반복문 - for 문, while 문, do-while 문
for 문 - 가장 많이 사용하는 반복문

중첩 반복
반복문이 또다른 반복문을 내포하고 있는 것


## 4월 5일 강의
배열 리언
배열의 레퍼런스만 리턴(배열 전체가 리턴되는 것이 아님)

메소드의 리턴 타입
리턴하는 배열의 타입과 리턴 받는 배열 타입 일치
리턴 타입에 배열의 크기를 지정하지 않음

예외(Exception)
- 실행 중 오동작이나 결과에 악영향을 미치는 예상치 못한 상황 발생
자바에서는 실행 중 발생하는 에러를 예외로 처리
- 실행 중 예외가 발생하면
자바 플랫폼은 응용프로그램이 예외를 처리하도록 호출
응용프로그램이 예외를 처리하지 않으면 프로그램 강제 종료 시킴
- 예외 발생 경우
정수를 0으로 나누는 겨웅
배열의 크기보다 큰 인덱스로 배열의 원소를 접근하는 경우
정수를 읽는 코드가 실행되고 있을 때 사용자가 문자를 입력한 경우

캡슐화
객체를 캡슐로 싸서 내부를 볼 수 없게 하는 것
객체의 가장 본질적인 특징은 외부의 접근으로부터 객체 보호
* 쉽게 생각하자면 붕어빵 생각하면 됌 !!
캡슐 = 붕어빵 껍데기, 객체 = 팔

자바의 캡슐화 
클래스(class):객체 모양을 선언한 틀(캡슐화 하는 틀)

자바의 객체 지향 특성
상속
상위 개체의 속성이 하위 개체에 물려짐
하위 개체가 상위 개체의 속성을 모두 가지는 관계

자바 상속
상의 클래스의 멤버를 하위 클래스가 물려받음
상위 클래스:슈퍼 클래스, 하위 클래스:서브 클래스(슈퍼 클래스 코드의 재사용, 새로운 특성 추가 가능)

객체 지향 언어의 목적
소프트웨어의 생산성 향상
컴퓨터 산업 발전에 따라 소프트웨어의 생명 주기(life cycle) 단축
소프트웨어를 빠른 속도로 생산한 필요성 증대

객체 지향 언어
- 상속, 다형성, 객체, 캡슐화 등 소프트웨어 재사용을 위한 여러 장치 내장
- 소프트웨어 재사용과 부분 수정 빠름
- 소프트웨어를 다시 만드는 부담 대폭 줄임
- 소프트웨어 생산성 향상

실세계에 대한 쉬운 모델링
- 초기 프로그래밍
수학 계산/통계 처리를 하는 등 처리 과정, 계산 절차 중요

- 현대 프로그래밍
컴퓨터가 산업 발전에 활용
실세계에서 발생하는 일을 프로그래밍
실세계에서는 절차나 과정보가 물체(객체)들의 상호 작용으로 묘사하는 것이 용이

- 객체 지향 언어
실세계의 일을 보다 쉽게 프로그래밍하기 위한 객체 중심적 언어

절차 지향 프로그래밍
작업 순서를 표현하는 컴퓨터 명령 집합
함수들의 집합으로 프로그램 작성
객체 지향 프로그래밍
컴퓨터가 수행하는 작업을 객체들간의 상호 작용으로 표현
클래스 혹은 객체들의 집합으로 프로그램 작성


클래스
객체의 속성(state)과 행위(behavior) 선언
객체의 설계도 혹은 틀

객체
클래스의 틀로 찍어낸 실체
- 프로그램 실행 중에 생성되는 실체 
- 메모리 공간을 갖는 구체적인 실체
- 인스턴스(instance)라고도 부름

자바 클래스 구성
클래스 
class 키워드로 선언
멤버 : 클래스 구성 요소
필드(멤버 변수)와 메소드(멤버 함수)
클래스에 대한 public 접근 지정:다른 모든 클래스에서 클래스 사용 허락
멤버에 대한 public 접근 지정 : 다른 모든 클래스에게 멤버 접근 허용

메소드
메소드는 C/C++의 함수와 동일
자바의 모든 메소드는 반드시 클래스 안에 있어야 함(캡슐화 원칙)

접근 지정자
- 다른 클래스에서 메소드를 접근할 수 있는지 여부 선언
- public, private, protected, 디폴트(접근 지정자 생략)
리턴 타입
메소드가 리턴하는 값의 데이터 타입

객체 소멸
- new에 의해 할당 받은 객체와 배열 메모리를 자바 가상 기계로 되돌려 주는 행위
- 소멸된 객체 공간은 가용 메모리에 포함

자바에서 사용자 임의로 객체 소멸 안됨
자바는 객체 소멸 연산자 없음
객체 생성 연산자:new
객체 소멸은 자바 가상 기계의 고유한 역할
자바 개발자에게는 매우 다행스러운 기능
C/C++에서는 할당 받은 객체를 개발자가 프로그램 내에서 삭제해야 함
C/C++의 프로그램 작성을 어렵게 만드는 요인
자바에서는 사용하지 않는 객체나 배열을 돌려주는 코딩 책임으로부터 개발자 해방


접근 지정자
자바의 접근 지정자
4가지
- private, protected, public, 티폴트(접근지정자 생략)

접근 지정자의 목적
클래스나 일부 멤버를 공개하여 다른 클래스에서 접근하도록 허용
객체 지향 언어의 캡슐화 정책은 멤버를 보호하는 것
접근 지정은 캡슐화에 묶인 보호를 일부 해제할 목적

클래스 접근 지정
다른 클래스에서 사용하도록 허용할 지 지정
public 클래스
다른 모든 클래스에게 접근 허용
디폴트 클래스(접근지정자 생략)
package-private라고도 함
같은 패키지의 클래스에만 접근 허용

## 04월 12일 강의
static 멤버의 생성
static 멤버는 클래스당 하나만 생성
객체들에 의해 공유됨



static 멤버 사용
- 클래스 이름으로 접근 가능
- 객체의 멤버로 접근 가능
- non-static 멤버는 클래스 이름으로 접근 안됨

final 클래스와 메소드
final 클래스 - 더 이상 클래스 상속 불가능
final 메소드 - 더 이상 오버라이딩 불가능


슈퍼 클래스의 멤버에 대한 서브 클래스의 접근
 
슈퍼 클래스의 private 멤버
- 서브 클래스에서 접근할 수 없음

슈퍼 클래스의 디폴트 멤버
- 서브 클래스가 동일한 패키지에 있을 때, 접근 가능

슈퍼 클래스의 public 멤버
- 서브 클래스는 항상 접근 가능

슈퍼 클래스의 protected 멤버
- 같은 패키지 내의 모든 클래스 접근 허용


protected 멤버
protected 멤버에 대한 접근
같은 패키지의 모든 클래스에게 허용
상속되는 서브 클래스(같은 패키지든 다른 페키지든 상관 없음)에게 허용

업캐스팅
기본 클래스의 포인터로 파생 클래스의 객체를 가리키는 것
한 곳을 가리키면 다른 곳은 가리킬 수 없다
- 서브 클래스의 레퍼런스를 슈퍼 클래스 레퍼런스에 대입
- 슈퍼 클래스 레퍼런스로 서브 클래스 객체를 가리키게 되는 현상 * 슈퍼클래스 레퍼런스로 객체 내의 슈퍼 클래스의 멤버만 접근 가능

다운캐스팅
- 슈퍼 클래스 레퍼런스를 서브 클래스 레퍼런스에 대입
- 업캐스팅된 것을 다시 원래대로 되돌리는 것
- 반드시 명시적 타입 변환 지정
업캐스팅 레퍼런스로는 객체의 실제 타입을 구분하기 어려움

instanceof 연산자
레퍼런스가 가리키는 객체의 타입 식별
객체레퍼런스 instanceof 클래스타입

서브 클래스 객체와 오버라이딩 된 메소드 호출
- 오버라이딩한 메소드가 실행됨을 보장


추상 클래스
추상 메소드
abstract로 선언된 메소드, 메소드의 코드는 없고 원형만 선언

추상 클래스
추상 메소드를 가지며, abstract로 선언된 클래스
추상 메소드 없이, abstract로 선언한 클래스


## 04월 19일 강의
추상 클래스의 상속과 구현
추상 클래스 상속
- 추상 클래스를 상속 받으면 추상 클래스가 됨

추상 클래스의 목적
- 상속을 위한 슈퍼 클래스로 활용하는 것
- 서브 클래스에서 추상 메소드 구현
- 다형성 실현

자바의 인터페이스
- 클래스가 구현해야 할 메소드들이 선언되는 추상형
- 인터페이스 선언(interface 키워드로 선언)  
자바 인터페이스에 대한 변화  
- java 7까지(인터페이스는 상수)
- java 8부터(상수와 추상메소드 포함, default, private, static 메소드 포함)  
여전히 인터페이스에는 필드(멤버 변수) 선언 불가  

인터페이스 간에 상속 가능  
인터페이스를 상속해 확장된 인터페이스 작성 가능  
extends 키워드로 상속 선언  
  
### 자바의 패키지와 모듈이란?  
패키지(package)  
서로 관련된 클래스와 인터페이스를 컴파일한 클래스 파일들을 묶어 놓은 디렉터리  
하나의 응용프로그램은 한 개 이상의 패키지로 작성  
패키지는 jar 파일로 압축 가능  
모듈(module)  
여러 패키지와 이미지 등의 자원을 모아 높은 컨테이너  
Java 9부터 모듈화 도입  
플랫폼의 모듈화 
Java 9부터 자바 API의 모든 클래스들(자바 실행 환경)을 패키지 기반에서 모듈들로 완전히 재구성  
응용프로그램의 모듈화  
- 클래스들은 패키지로 만들고, 다시 패키지를 모듈로 많듦
- 모듈 프로그래밍은 어렵고 복잡, 기존 방식으로 프로그램 작성  
  

모듈화의 목적  
Java 9부터 자바 API를 여러 모듈(99개)로 분할  
- Java 8까지는 rt.jar의 한 파일에 모든 API 저장  
  
응용프로그램이 실행할 때 꼭 필요한 모듈들로만 실행 환경 구축  
- 메모리 자원이 열악한 작은 소형 기기에 꼭 필요한 모듈로 구성된 작은 크기의 실행 이미지를 만들기 위함  
  
모듈의 현실  
- Java 9부터 전면적으로 도입
- 복잡한 개념
- 큰 자바 응용프로그램에는 개발, 유지보수 등에 적합
- 현실적으로 모듈로 나누어 자바 프로그램을 작성할 필요 없음  
  
다른 패키지에 작성된 클래스 사용  
import를 이용하지 않는 경우  
- 소스에 클래스 이름의 완전 경로명 사용  
  
필요한 클래스만 import  
- 소스 시작 부분에 클래스의 경로명 import  
- import 패키지.클래스
- 소스에는 클래스 명 명시하면 됨
- 
## 05월 03일 강의
컬렉션  
요소라고 불리는 가변 개수의 객체들의 저장소
- 객체들의 컨테이너라고도 불림
- 요소의 개수에 따라 크기 자동 조절

컬렉션은 제너릭 기법으로 구현
      
제네릭  
- 특정 타입만 다루지 않고, 여러 종류의 타입으로 변신할 수 있도록 클래스나
메소드를 일반화시키는 기법
제네릭 컬렉션 사례:벡터
- <E>에서 E에 구체적인 타입을 주어 구체적인 타입만 다루는 벡터로 활용
- 정수만 다루는 컬렉션 벡터 Vector<Integer>
- 문자열만 다루는 컬렉션 벡터 Vector<String>

컬렉션의 요소는 객체만 가능
- int, char, double 등의 기본 타입으로 구체화 불가

벡터 Vector<E>의 특성
- <E>에 사용할 요소의 특정 타입으로 구체화
- 배열을 가변 크기로 다룰 수 있게 하는 컨테이너
  - 배열의 길이 제한 극복
  - 요소의 개수가 넘치면 자동으로 길이 조절
- 요소 객체들을 삽입, 삭제, 검색하는 컨테이너
  - 삽입, 삭제에 따라 자동으로 요소의 위치 조정


HashMap<K, V>
키(key)와 값(value)의 쌍으로 구성되는 요소를 다루는 컬렉션  
- K:키로 사용할 요소의 타입
- V:값으로 사용할 요소의 타입
- '값'을 검색하기 위해서는 반드시 '키' 사용

삽입 및 검색이 빠른 특징
- 요소 삽입:put() 메소드
- 요소 검색:get() 메소드

컨테이너와 컴포넌트
컨테이너  
- 다른 컴퓨넌트를 포함할 수 있는 GUI 컴포넌트
  - java.awt.Container를 상속받음
- 다른 컨테이너에 포함될 수 있음
  - AWT 컨테이너 : Panel, Frame, Applet, Dialog, Window
  - Swing 컨테이너 : JPanel JFrame, JApplet, JDialog, JWindow

컴포넌트  
- 컨테이너에 포함되어야 화면에 출력될 수 있는 GUI 객체
- 다른 컴포넌트를 포함할 수 없는 순수 컴포넌트
- 모든 GUI 컴포넌트가 상속받는 클래스 : java.awt.Component
- 스윙 컴포넌트가 상속받는 클래스 : javax.swing.JComponent

최상위 컨테이너
- 다른 컨테이너에 포함되지 않고도 화면에 출력되며 독립적으로 존재 가능한 컨테이너
  - 스스로 화면에 자신을 출력하는 컨테이너 : JFrame, JDialog, JApplet


## 05월 17일
배치 관리자 대표 유형 4가지  
FlowLayout 배치관리자  
- 컴포넌트가 삽입되는 순서대로 왼쪽에서 오른쪽으로 배치  
- 배치할 공간이 없으면 아래로 내려와서 반복한다. 
   
BorderLayout 배치관리자  
- 컨테이너의 공간을 동, 서, 남, 북, 중앙의 5개 영역으로 나눔
  
GridLayout 배치관리자  
- 컨테이너를 프로그램에서 설정한 동일한 크기의 2차원 격자로 나눔
- 컴포넌트는 삽입 순서대로 좌에서 우로, 다시 위에서 아래로 배치
  
CardLayout  
- 컨테이너의 공간에 카드를 쌓아놓은 듯이 컴포넌트를 포개어 배치


스윙 응용프로그램의 종료
응용프로그램 내에서 스스로 종료하는 방법  
System.exit(0);  
언제 어디서나 무조건 종료  
  
프레임의 오른쪽 상단의 종료버튼(X)이 클릭되면 어떤 일이 일어나는가?  
프레임 종료, 프레임 윈도우를 닫음(프레임이 화면에서 보이지 않게 됨)  
프레임이 보이지 않게 되지만 응용프로그램이 종료한 것은 아님(키보드나 마우스 입력을 받지 못함, 다시 setVisible(true))를 호출하면, 보이게 되고 이전 처럼 작동함  

프레임 종료버튼이 클릭될 때, 프레임과 함께 프로그램을 종료시키는 방법  
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);    
  
BorderLayout 생성자와 add()메소드  
생성자  
- BorderLayout()
- BorderLayout(int hGap, int yGap)  
  - hGap(좌우 두 컴포텉트 사이의 수평 간격, 픽셀 단위, 디폴트:0)
  - yGap(상하 두 컴포넌트 사이의 수직 간격, 픽셀 단위, 디폴트:0)  
    
add()메소드  
- void add(Componenet comp, int index)
  - comp 컴포넌트를 index 위치에 삽입한다.
  - index : 컴포넌트의 위치  
  동:BorderLayout.EAST, 서:BorderLayout.WEST, 남:borderLayout.SOUTH, 북:BorderLayout.NORTH, 중앙:BorderLayout.CENTER

컴포넌트의 절대 위치와 크기 설정  
배치 관리자가 없는 컨테이너에 컴포넌트를 삽입할 때
- 프로그램에서 컴포넌트의 절대 크기와 위치 설정
- 컴포넌트들이 서로 겹치게 할 수 있음

컴포넌트의 크기와 위치 설정 메소드
- void setSize(int width, int height) // 컴포넌트 크기 설정
- void setLocation(int x, int y) // 컴포넌트 위치 설정
- void setBounds(int x, int y, int width, int height) // 위치와 크기 동시 설정



## 05월 24일  
이벤트 기반 프로그래밍
- 이벤트 기반 프로그래밍  
  - 이벤트가 발생하면 이벤트를 처리하는 루틴(이벤트 리스너) 실행
  - 실행될 코드는 이벤트의 발생에 의해 전적으로 결정
- 반대되는 개념 : 배치 실행  
  - 프로그램의 개발자가 프로그램의 흐름을 결정하는 방식
- 이벤트 종류
  - 사용자의 입력 : 마우스 드래그, 마우스 클릭, 키보드 누름 등 
  - 센서로부터의 입력, 네트워크로부터 데이터 송수신
  - 다른 응용 프로그램이나 다른 스레드로부터의 메시지
- 이벤트 기반 응용 프로그램의 구조
  - 각 이벤트마다 처리하는 리스너 코드 보유
- GUI 응용프로그램은 이벤트 기반 프로그래밍으로 작성됨
  - GUI 라이브러리 종류
    - C++의 MFC, C# GUI, Visual Basic, X Window, Android 등
    - 자바의 AWT와 Swing

자바 스윙 프로그램에서 이벤트 처리 과정  
- 이벤트가 처리되는 과정
  - 이벤트 발생
      - 예 : 마우스의 움직임 혹은 키보드 입력
  - 이벤트 객체 생성
      - 현재 발생한 이벤트에 대한 정보를 가진 객체
  - 응용프로그램에 작성된 이벤트 리스너 찾기
  - 이벤트 리스너 실행
    - 리스너에 이벤트 객체 전달
    - 리스너 코드 실행

이벤트 객체
- 발생한 이벤트에 관한 정보를 가진 객체
- 이벤트 리스너에 전달됨
  - 이벤트 리스너 코드가 발생한 이벤트에 대한 상황을 파악할 수 있게 함  
    

- 이벤트 객체가 포함하는 정보
  - 이벤트 종류와 이벤트 소스
  - 이벤트가 발생한 화면 좌표 및 컴포넌트 내 좌표
  - 이벤트가 발생한 버튼이나 메뉴 아이템의 문자열
  - 클릭된 마우스 버튼 번호 및 마우스의 클릭 횟수
  - 키의 코드 값과 문자 값
  - 체크박스, 라디오버튼 등과 같은 컴포넌트에 이벤트가 발생하였다면 체크 상태

- 이벤트 소스를 알아 내는 메소드
  - Object getSource()
    - 발생한 이벤트의 소스 컴포넌트 리턴
    - Object 타입으로 리턴하므로 캐스팅하여 사용
    - 모든 이벤트 객체에 대해 적용

리스너 인터페이스
- 이벤트 리스너
  - 이벤트를 처리하는 자바 프로그램 코드, 클래스로 작성,
- 자바는 다양한 리스너 인터페이스 제공
  - 예) ActionLister 인터페이스 - 버튼 클릭 이벤트를 처리하기 위한 인터페이스
  - 예) MouseListter 인터페이스 - 마우스 조작에 따른 이벤트를 처리하기 위한 인터페이스
- 사용자의 이벤트 리스너 작성
  - 자바의 리스너 인터페이스(interface)를 상속받아 구현
  - 리스너 인터페이스의 모든 추상 메소드 구현

이벤트 리스너 작성 과정 사례
1. 이벤트와 이벤트 리스너 선택
  - 버튼 클릭을 처리하고자 하는 경우
    - 이벤트 : Action 이벤트, 이벤트 리스너 : ActionListener
2.  이벤트 리스너 클래스 작성 : ActionListener 인터페이스 구현
3. 리벤트 리스너 등록
  - 이벤트를 받아 처리하고자 하는 컴포넌트에 이벤트 리스너 등록
  - component.addXXXListener(listener)
    - xxx : 이벤트 명, listener : 이벤트 리스너 객체

이벤트 리스너 작성 방법
- 3가지 방법
  - 독립 클래스로 작성
    - 이벤트 리스너를 완전한 클래스로 작성
    - 이벤트 리스너를 여러 곳에서 사용할 때 적합
  - 내부 클래스(inner class)로 작성
    - 클래스 안에 멤버처럼 클래스 작성
    - 이벤트 리스너를 특정 클래스에서만 사용할 때 적합
  - 익명 클래스(annoymous class)로 작성
    - 클래스의 이름 없이 간단히 리스너 작성
    - 클래스 조차 만들 필요 없이 리스너 코드가 간단한 경우에 적합

익명 클래스로 이벤트 리스너 작성
- 익명 클래스(annoymous class) : 이름 없는 클래스
  - (클래스 선언 + 인스턴스 생성)을 한번에 달성
  - 간단한 리스너의 경우 익명 클래스 사용 추천
    - 메소드 개수가 1, 2개인 리스너(ActionListener, ItemListener)에 대해 주로 사용 

어댑터 클래스
- 이벤트 리스너 구현에 따른 부담
  - 리스너의 추상 메소드를 모두 구현해야 하는 부담
  - 예) 마우스 리스너에서 마우스가 눌려지는 경우(mousePressed())만 처리하고자 하는 경우에도 나머지 4개의 메소드를 모두 구현해야 하는 부담
- 어댑터 클래스(Adapter)
  - 리스너의 모든 메소드를 단순 리턴하도록 만든 클래스(JDK에서 제공)
- 추상 메소드가 하나뿐인 리스너는 어댑터 없음
  - ActionAdapter, ItemAdapter 클래스는 존재하지 않음

Key 이벤트와 포커스
- 키 입력 시, 다음 세 경우 각각 Key 이벤트 발생
  - 키를 누르는 순간
  - 누른 키를 떼는 순간
  - 누른 키를 떼는 순간(Unicode 키의 경우에만)
- 키 이벤트를 받을 수 있는 조건
  - 모든 컴포넌트
  - 현재 포커스(focus)를 가진 컴포넌트가 키 이벤트 독점
- 포커스(focus)
  - 컴포넌트나 응용프로그램이 키 이벤트를 독점하는 권한
  - 컴포넌트에 포커스 설정 방법 : 다음2 라인 코드 필요

KeyListener  
- 응용프로그램에서 KeyListener를 상속받아 키 리스너 구현
- KeyListener의 3개 메소드
1. void KeyPressed(KeyEvent e) {
  // 이벤트 처리 루틴
}
2. void KeyReleased(KeyEvent e) {
  // 이벤트 처리 루틴
}
3. void KeyTyped(KeyEvent e) {
  // 이벤트 처리 루틴
}

유니코드 키의 특징
- 국제 산업 표준
- 전 세계의 문자를 컴퓨터에서 일관되게 표현하기 위한 코드 체계
- 문자들에 대해서만 키 코드 값 정의
  - A~Z, a~z, 0~9, !@& 등
- 문자가 아닌 키 경우에는 표준화된 키 코드 값 없음
  - <Function> 키, <Home> 키, <UP> 키, <Delete> 키,<Control> 키, <Shift> 키, <ALT> 등은 플랫폼에 따라 키 코드 값이 다를 수 있음

- 유니코드 키가 입력되는 경우
  - KeyPressed(), KeyTyped(), KeyReleased()가 순서대로 호출
- 유니코드 키가 아닌 경우
  - KeyPressed(), KeyReleased()만 호출됨


가상 키와 입력된 키 판별
- KeyEvent 객체
  - 입력된 키 정보를 가진 이벤트 객체
  - KeyEvent 객체의 메소드로 입력된 키 판별
- keyEvent 객체의 메소드로 입력된 키 판별
  - char keyEvent.getKeyChar()
    - 키의 유니코드 문자 값 리턴
    - Unicode 문자 키인 경우에만 의미 있음
    - 입력된 키를 판별하기 위해 문자 값과 비교하면 됨
- int KeyEvent.getKeyCode()
  - 유니코드 키 포함
  - 모든 키에 대한 정수형 키 코드 리턴
  - 입력된 키를 판별하기 위해 가상키(Virtual) 값과 비교해야 함
  - 가상 키 값은 KeyEvent 클래스에 상수로 선언


마우스 리스너 달기와 MouseEvent 객체 활용
- 마우스 리스너 달기
  - 마우스 리스너는 컴포넌트에 다음과 같이 등록(conponent.addMouseListener(myMouseListener);)
  - 컴포넌트가 마우스 무브(mouseMoved())나 마우스 드래깅(mouseDragged())을 함께 처리하고자 하면, MouseMotion 리스너 따로 등록(component.addMouseMotionListener(myMouseMotionListener);)
- MouseEvent 객체 활용
  - 마우스 포인터의 위치, 컴포넌트 내 상대 위치
    - int getX(), int getY()
  - 마우스 클릭 횟수
    - int getClickCount()

## 05월 31일
자바의 GUI 프로그래밍 방법  
- 자바의 GUI 프로그래밍 방법 2 종류
  - 컴포넌트 기반 GUI 프로그래밍
    - 스윙 컴포넌트를 이용하여 쉽게 GUI를 구축
    - 자바에서 제공하는 컴포넌트의 한계를 벗어나지 못함
  - 그래픽 기반 GUI 프로그래밍
    - 그래픽을 이용하여 GUI 구축
    - 개발자가 직접 그래픽으로 화면을 구성하는 부담
    - 독특한 GUI를 구성할 수 있는 장점
    - GUI처리의 실행 속도가 빨라, 게임 등에 주로 이용

스윙 컴포넌트의 공통 메소드, JComponent의 메소드  
- JComponent
  - 스윙 컴포넌트는 모두 상속받는 슈퍼 클래스, 추상 클래스
  - 스윙 컴포넌트들이 상속받는 공통 메소드와 상수 구현
  - JComponent의 주요 메소드 사례
        

컴포넌트의 모양과 관련된 메소드  
void setForeground(Color) 전경색 설정  
void setBackground(Color) 배경색 설정  
void setOpaque(boolean) 불투명성 설정  
void setFont(Font) 폰트 설정  
Font getFont() 폰트 리턴  

컴포넌트의 상태와 관련된 메소드
void setEnabled(boolean) 컴포넌트 활성화/비활성화
void set Visible(boolean) 컴포넌트 보이기/숨기기
boolean isvisible() 컴포넌트의 보이는 상태 리턴  
  
컴포넌트의 위치와 크기에 관련된 메소드
int getWidth() 폭 리턴  
int getHeight() 높이 리턴  
int getX() x 좌표 리턴  
int getY() y 좌표 리턴  
Point getLocationOnScreen() 스크린 좌표상의 컴포넌트 좌표  
void setLocation(int, int) 위치 지정  
void setSize(int, int) 크기 지정
  
컨테이너를 위한 메소드  
Component add(Component) 자식 컴포넌트 추가  
void remove(Component) 자식 컴포넌트 제거  
void removeALL() 모든 자식 컴포넌트 제거  
Component[] getComponents() 자식 컴포넌트 배열 리턴  
Container getParent() 부모 컨테이너 리턴  
Container getTopLeveLAncestor() 최상위 부모 컨테이너 리턴  
  
JLabel로 문자열과 이미지 출력  
- JLabel의 용도  
  - 문자열이나 이미지를 화면에 출력하기 위한 목적  
- 레이블 생성 
JLabel() 빈 레이블  
JLabel(Icon image) 이미지 레이블  
JLabel(String text) 문자열 레이블  
JLabel(String text, ICon image, int hAlign) 문자열과 이미지 모두 가진 레이블   
.hAlign : 수평 정렬 값으로 ScingConstants.LEFT, SwingConstants.RIGHT,SwingConstants.CENTER 중 하나  

레이블 생성 예  
- 문자열 레이블 생성  
JLabel textLabel = new JLabel("사랑합니다");  
  
- 이미지 레이블 생성  
  - 이미지 파일로부터 이미지를 읽기 위해 ImageIcon 클래스 사용  
  - 다룰 수 있는 이미지 : png, gif, jpg  
    - sunset.jpg의 경로명이 "images/sunset.jpg"인 경우  
    ImageIcon image = new ImageIcon(images/suset.jpg");  
    JLabel imageLabel = new JLabel(image);  
  
  - 수평 정렬 값을 가진 레이블 컴포넌트 생성  
    - 수평 정렬로, 문자열과 이미지를 모두 가진 레이블  
    ImageIcon image = new ImageIcon("images/sunset.jpg");
    JLabel label = new JLabel("사랑합니다", image, SwingConstants.CENTER);  
  
  
이미지 버튼 만들기  
- 하나의 버튼에 3개의 이미지 등록
  - 마우스 조작에 따라 3개의 이미지 중 적절한 이미지 자동 출력  
- 3개의 버튼 이미지  
  - normalIcon  
    - 버튼의 보통 상태(디폴트) 때 출력되는 이미지  
    - 생성자에 이미지 아이콘 전달 혹은 JButton의 setIcon(normalIcon);  
  - rolloverIcon  
    - 버튼에 마우스가 올라갈 때 출력되는 이미지  
    - 이미지 설정 메소드 : JButton의 setRolloverIcon(rollOverIcon);  
  - pressdIcon  
    - 버튼을 누른 상태 때 출력되는 이미지   
    - 이미지 설정 메소드 : JButton의 setPressedIcon(pressedIcon)  


체크박스에 Item 이벤트 처리
- Item 이벤트  
  - 체크 박스의 선택 상태에 따라 변화가 생길 때 발생하는 이벤트  
    - 사용자가 마우스나 키보드를 선택/해제할 때  
    - 프로그램에서 체크박스를 선택/해제하여 체크 상태에 변화가 생길 때  
    JCheckBox c = new JCheckBox("사과");
    c.setSelect(true); // 선택 상태로 변경  
    - 이벤트가 발생하면 ItemEvent 객체 생성
    - ItemListener 리스너를 이용하여 이벤트 처리
- ItemListener 리스너의 추상 메소드  
void itemStateChanged(ItemEvent e) 체크박스의 선택 상태가 변하는 경우 호출   
- ItemEvent의 주요 메소드   
it getStateChange() 체크박스가 선택된 경우 ItemEvent.SELECTD를, 해제된 경우 ItemEvent.DESELECTED를 리턴한다.  
Object getItem() 이벤트를 발생시킨 아이템 객체를 리턴한다. 체크박스의 경우 JCheckBox 컴포넌트의 레퍼런스를 리턴한다.  

JRadioButton으로 라디오버튼 만들기  
JRadioButton의 용도  
- 버튼 그룹을 형성하고, 그룹에 속한 버튼 중 하나만 선택되는 라디오버튼  
- 체크박스와의 차이점  
  - 체크 박스는 각각 선택/ 해체가 가능하지만, 라디오버튼은 그룹에 속한 버튼 중 하나만 선택  
  
라디오버튼 생성  
JRadioButton() 빈 라디오버튼  
JRadioButton(Icon image) 이미지 라디오버튼  
JRadioButton(Icon image, boolean selected) 이미지 라디오버튼  
JRadioButton(String text) 문자열 라디오버튼  
JRadioButton(String text, boolean selected) 문자열 라디오버튼  
JRadioButton(String text, Icon image) 문자열과 이미지를 가진 라디오버튼  
JRadioButton(Sting text, Icon image, boolean selected) 문자열과 이미지를 가진 라디오버튼  
.selected:true면 선택 상태로 초기화  

  
라디오버튼 생성 및 Item 이벤트 처리  
- 버튼 그룹과 라디오버튼 생성 과정  
1. 버튼 그룹 객체 생성  
ButtonGroup group = new ButtonGroup();  
2. 라디오버튼 생성  
JRadioButton apple = new JRadioButton("사과");  
JRadioButton pear = new JRadioButton("배");  
JRadioButton cherry = new JRadioButton("체리")
3. 라디오버튼을 버튼 그룹에 삽입  
group.add(apple);  
container.add(pear);  
container.add(cherry);  
  
- 라디오버튼에 Item 이벤트 처리 : ItemListener 리스너 이용  
  - 라디오버튼이 선택/해제되어 상태가 달라지면, item 이벤트 발생  
    - 사용자가 마우스나 키보드로 선택 상태를 변경할 때  
    - 프로그램에서 JRadioButton이 setSelected()를 호출하여 선택 상태를 변경할 때  

  
JTextField로 한 줄 입력 창 만들기  
- JTextField  
  - 한 줄의 문자열을 입력 받는 창(텍스트필드)  
     - 텍스트 입력 도중 <Enter> 키가 입력되면 Action 이벤트 발생
     - 입력 가능한 문자 개수와 입력 창의 크기는 서로 다름  
  - 텍스트필드 생성  
  JTextField() 빈 텍스트필드  
  JTextField(int cols) 입력 창의 열의 개수가 cols개인 텍스트필드  
  JTextField(String text) text 문자열로 초기화된 텍스트필드  
  JTextFiels(String text, int cols) 입력 창의 열의 개수는 cols개이고 text 문자열로 초기화 된 텍스트필드  
  - "컴퓨터공학과"로 초깃값을 가지는 텍스트필드 생성 예  
  JTextField tf2 = new JTextField("컴퓨터공학과");  

  
텍스트영역 생성 예  
"hello" 문자열의 초깃값을 가지고, 한 줄에 20개의 문자가 입력 가능하며, 7줄로 구성된 텍스트 영역 만들기  
JTextArea ta = new JTextArea("hello", 7, 20);  
container.add(ta);  
왼쪽에 만든 텍스트영역에 스크롤바 붙이기  
JTextArea ta = new JTextArea("hello", 7, 20);  
container.add(new JScrollPane(ta));  

JComboBox<E>  
- JComboBox<E>  
  - 텍스트필드와 버튼, 그리고 드롭다운 리스트로 구성되는 콤보박스  
  - 드롭다운 리스트에서 선택한 것이 텍스트필드에 나타남  
- 콤보박스 생성  
JComboBox<E>()빈 콤보박스  
JComboBox<E>(Vector listData) 벡터로부터 아이템을 공급받는 콤보박스
JComboBox<E>(Object [] ListData) 배열로부터 아이템을 공급받는 콤보박스  
예) 텍스트를 아이템으로 가진 콤보박스 생성  
String [] fruits = {"apple", "banana", "kiwi", "mango", "pear" ,"peach", "berry", "strawberry", "blackberry"};  
JComboBox<String> combo = new JComboBox<String>(fruits);  

메뉴 구성  
- 메뉴 만들기에 필요한 스윙 컴포넌트
  - 메뉴아이템 - JMenuItem  
  - 메뉴 - JMenu  
    - 여러 개의 메뉴 아이템을 가짐  
  - 메뉴바 - JMenuBar  
    - 여러 개의 메뉴를 붙이는 바이며 프레임에 부착됨  
  - 분리선  
    - 메뉴아이템 사이의 분리선으로 separator라고 부름  
    - JMenu의 addSeparator()를 호출하여 삽입함  
  
메뉴아이템에 Action 이벤트 달기  
- 메뉴아이템을 클릭하면 Action 발생  
  - 메뉴아이템은 사용자로부터의 지시나 명령을 받는데 사용  
  - ActionListener 인터페이스로 리스너 작성
  - 각 메뉴아이템마다 이벤트 리스너 설정  

예) Load 메뉴아이템에 Action 리스너를 작성하는 경우  
JMenuItem item = new JMenuItem("Load");  
item.addActionListener(new MenuActionListener()); // 메뉴아이템에 Action 리스너 설정  
screenMenu.add(item);  

class.MenuActionListener implements ActionListener {
  public void actionPerformed(ActionEvent e) {
    // 사용자가 Load 메뉴아이템을 선택하는 경우 처리할 작업 구현  
    ...
  }
}  


팝업 다이얼로그, JOptionPane  
- 팝업 다이얼로그  
  - 사용자에게 메시지를 전달하거나 문자열을 간단히 입력받는 용도  
  - JOptionPane 클래스를 이용하여 생성  
    - static 타입의 간단한 메소드 이용  
  - 입력 다이얼로그 - JOptionPane.showInputDialog()  
    - 한 줄을 입력 받는 다이얼로그  
    static String JOptionPane.showInputDialog(String msg)  
    . msg : 다이얼로그 메시지  
    . 리턴 값 : 사용자가 입력한 문자열, 취고 버튼이 선택되거나 창이 닫히면 null 리턴  
      

확인 다이얼로그  
- 확인 다이얼로그 - JOptionPane.showConfirmDialog()  
  - 사용자로부터 Yes/No 응답을 입력 받는 다이얼로그  
static int JOptionPane.showConfirmDialog(component parentCompoenet, Object msg, String title, int optionType)  
. ParentComponent : 다이얼로그의 부모 컴포넌트로서 다이얼로그가 출력되는 영역의 범위 지정을 위해 사용(예 : 프레임) .null이면 전체 화면 중앙에 출력  
. msg : 다이얼로그 메시지  
. title : 다이얼로그 타이틀  
. optionType : 다이얼로그 옵션 종류 지정(YES_NO_OPTION, YESNO CANCEL_OPTION, OK_CANCEL_OPTION)  
. 리턴 값 : 사용자가 선택한 옵션 종류(YES_OPTION, NO_OPTION, CANCEL_OPTION, CLOSED_OPTION)  

## 06월 07일
스윙 컴포넌트 그리기, paintComponent()  
- 스윙의 페인팅 기본  
  - 모든 컴포넌트는 자신의 모양을 스스로 그린다.
  - 컨테이너는 자신을 그린 후 그 위에 자신 컴포넌트들에게 그리기 지시  
  - 모든 스윙 컴포넌트는 자신의 모양을 그리는 paintComponent() 메소드 보유  
- public void paintComponent(Graphics g)  
  - 스윙 컴포넌트가 자신의 모양을 그리는 메소드  
  - JComponent의 메소드 : 모든 스윙 컴포넌트가 이 메소드를 오버라이딩함  
  - 언제 호출되는가?  
    - 컴포넌트가 그려져야 하는 시점마다 호출  
    - 크기가 변경되거나, 위치가 변경되거나, 컴포넌트가 가려졌던 것이 사라지는 등(개발자가 직접 호출하면 안 됨)
  - 매개변수인 Graphics 객체  
    - 그래픽 컨텍스트 : 컴포넌트 그리기에 필요한 도구를 제공하는 객체  
    - 자바 플랫폼에 의해 공급  
    - 색 지정, 도형 그리기, 글리핑, 이미지 그리기 등의 메소드 제공    

그래픽 기반 GUI 프로그래밍  
- 그래픽 기반 GUI 프로그래밍  
  - 스윙 컴포넌트에 의존하지 않고, 원 이미지 등을 이용하여 직접 화면을 구성하는 방법  
  - 그래픽 기반 GUI 프로그래밍의 학습이 필요한 이유  
    - 컴포넌트의 한계를 극복하고 차트, 게임 등 자유로운 콘택트 표현  
    - 그래픽은 컴포넌트에 비해 화면 출력 속도가 빠름  
    - 스윙 컴포넌트들로 모두 그래픽으로 작성되어 있어, 그래픽에 대한 학습은 자바 GUI의 바탕 기술을 이해하는데 도움  
    - 그래픽을 이용하여 개발자 자신만의 컴포넌트 개발   

그래픽의 색과 폰트  
- 색 : Color 클래스  
  - 자바의 색 : r(Red), g(Green), b(Blue) 성분으로 구성, 각 성분은 0~255(8비트) 범위의 정수  
  Color(int r, int g, int b) r, g, b 값으로 sRGB 색 생성  
  Color(int rgb) rgb는 32비트의 정수이지만, 하위 24비트만 유효. 즉, 0x00rrggbb로 표현. 각 바이트가 r, g, b의 색 성분  
  예) 빨간색 : new Color(255, 0, 0), 초록색 : new Color(0x0000ff00); 노란색 : Color.YELLOW  
- 폰트 : Font 클래스  
Font(String fontFace, int style, int size) 
- fontFace:"고딕체", "Ariel"등과 같은 폰트 이름  
- style:Font.BOLD, font.ITALIC, Font.PLAIN 중 한 값으로 문자의 스타일  
- size:픽셀 단위의 문자 크기  

- Graphics에 색과 폰트 설정  
void setColor(Color color) 그래픽 색을 color로 설정. 그리기 시에 색으로 이용  
void setFont(Font font) 그래픽 폰트를 font로 설정. 문자열 출력 시 폰트로 이용  

도형 그리기와 칠하기  
- 도형 그리기  
  - 선, 타원, 사각형, 둥근 모서리 사각형, 원호, 폐 다각형 그리기  
  - 선의 굵기 조절할 수 없음  
void drawLine(int x1, int y1, int x2, int y2) _ (x1, y1)에서 (x2, y2)까지 선을 그린다.  
void drawOval(int x, int y, int w, int h) _ (x, y)에서 w x h 크기의 사각형에 내접하는 타원을 그린다.  
void drawRecy(int x, int y, int w, int h) _ (x, y)에서 w x h 크기의 사각형을 그린다.  
void drawRoundRect(int x, int y, int w, int , int arcWidth, int arcHeight)  
- arcWidth : 모서리 원의 수평 반지름  
- arcHeight: 모서리 원의 수직 반지름 _ (x, y)에서 w x h 크기의 사각형을 그리되, 4개의 모서리는 arcwidth와 arcHeight를 이용하여 원호로 그린다.  

도형 칠하기 
- 도형을 그리고 내부를 칠하는 기능  
  - 도형의 외곽선과 내부를 따로 칠하는 기능 없음  
- 도형 칠하기를 위한 메소드  
  - 그리기 메소드 명에서 draw 대신 fill로 이름 대치하면 됨. fillRect(), fillOval() 등  


스윙에서 이미지를 그리는 2가지 방법  
1. JLabel을 이용한 이미지 그리기  
ImageIcon image = new Imageicon("images/apple.jpg");  
JLabel label = new JLabel(image);  
panel.add(label);  
장점 : 이미지 그리기 간편 용이  
단점 : 이미지의 원본 크기대로 그리므로 이미지 크기 조절 불가  

2. Graphics의 drawImage()로 이미지 출력  
장점 : 이미지 일부분 등 이미지의 원본 크기와 다르게 그리기 가능  
단점 : 컴포넌트로 관리할 수 없음, 이미지의 위치나 크기 등을 적절히 조절하는 코딩 필요  

repaint()  
- repaint()  
  - 모든 컴포넌트가 가지고 있는 메소드  
  - 자바 플랫폼에게 컴포넌트 그리기를 강제 지시하는 메소드  
  - repaint()를 호출하면, 자바 플랫폼이 컴포넌트의 paintComponent 호출(component.repaint();)  

- repaint()의 호출이 필요한 경우  
  - 개발자가 컴포넌트를 다시 그리고자 하는 경우  
    - 프로그램에서 컴포넌트의 모양과 위치를 변경하고 바로 화면에 반영시키고자 하는 경우  
    - 컴포넌트가 다시 그려져야 그 때 변경된 위치에 변경된 모양으로 출력됨  
    - repaint()는 자바 플랫폼에게 지금 당장 컴포넌트를 다시 그리도록 지시함  

- 부모 컴포넌트로부터 다시 그리는 것이 좋음  
  - 컴포넌트 repaint()가 불려지면  
    - 이 컴포넌트는 새로운 위치에 다시 그려지지만 이전의 위치에 있던 자신의 모양이 남아 있음  
  - 부모 컴포넌트의 repaint()를 호출하면  
    - 부모 컨테이너의 모든 내용을 지우고 자식을 다시 그리기 때문에 컴포넌트의 이전 모양이 지워지고 새로 변경된 크기나 위치에 그려짐  

 멀티태스킹(multi-tasking) 개념  
 - 멀티 태스킹  
  - 여러 개의 작업(태스크)이 동시에 처리 되는 것  

스레드와 운영체제  
- 스레드(thread)  
  - 운영체제에 의해 관리되는 하나의 작업 혹은 태스크  
  - 스레드와 태스크(혹은 작업은 바꾸어 사용해도 무관)  

- 멀티스레딩(multi-threading)
  - 여러 스레드를 동시에 실행시키는 응용프로그램을 작성하는 기법  

- 스레드 구성  
  - 스레드 코드  
    - 작업을 실행하기 위해 작성한 프로그램 코드  
    - 개발자가 작성  
  - 스레드 정보  
    - 스레드 명, 스레드 ID, 스레드의 실행 소요 시간, 스레드의 우선 순위 등  
    - 운영체제가 스레드에 대해 관리하는 정보  

멀티태스킹과 멀티스레딩  
- 멀티태스킹 구현 기술  
  - 멀티프로세싱(multi-processing)  
    - 하나의 응용프로그램이 여러 개의 프로세스를 생성하고, 각 프로세스가 하나의 작업을 처리하는 기법  
    - 각 프로세스 독립된 메모리 영역을 보유하고 실행  
    - 프로세스 사이의 문맥 교환에 따른 과도한 오버헤드와 시간 소모의 문제점  
  - 멀티스레딩(multi-threading)  
    - 하나의 응용프로그램이 여러 개의 스레드를 생성하고, 각 스레드가 하나의 작업을 처리하는 기법  
    - 하나의 응용프로그램에 속한 스레드는 변수 메모리, 파일 오픈 테이블 등 자원으로 공유하므로, 문맥 교환에 따른 오버헤드가 매주 작음  
    - 현재 대부분의 운영체제가 멀티스레딩을 기본으로 하고 있음  

자바 스레드(Thread)와 JVM  
- 자바 스레드  
  - 자바 가상 기계(JVM)에 의해 스케쥴되는 실행 단위의 코드 블럭  
  - 스레드의 생명 주기는 JVM에 의해 관리됨 : JVM은 스레드 단위로 스케쥴링  
  - JVM과 자바의 멀티스레딩  
    - 하나의 JVM은 하나의 자바 응용프로그램만 실행  
      - 자바 응용프로그램이 시작될 때 JVm이 함께 실행됨  
      - 자바 응용프로그램이 종료하면 JVM도 함께 종료함  
    - 응용프로그램은 하나 이상의 스레드로 구성 가능  
  
자바 스레드 만들기  
- 스레드 만드는 2 가지 방법  
  - java.lang.Thread 클래스를 상속받아 스레드 작성  
  - java.lang.Runnable 인터페스를 구현하여 스레드 작성  

Thread 클래스를 상속받아 스레드 만들기  
- Thread를 상속받아 run() 오버라이딩  
  - Thread 클래스 상속, 새 클래스 작성  
  - run() 메소드 작성  
    - run() 메소드를 스레드 코드라고 부름  
    - run() 메소드에서 스레드 실행 시작  

- 스레드 객체 생성  
    - 생성된 객체는 필드와 메소드를 가진 객체일 뿐 스레드로 작동하지 않음  


- 스레드 시작  
  - start() 메소드 호출  
    - 스레드로 작동 시작  
    - 스레드 객체의 run()이 비로소 실행  
    - JVM에 의해 스케쥴되기 시작함  

Runnable 인터페이스로 스레드 만들기  
- Runnable 인터페이스 구현하는 새 클래스 작성  
  - run() 메소드 구현  
    - run() 메소드를 스레드 코드라고 부름  
    - run() 메소드에서 스레드 실행 시작  

- 스레드 객체 생성  

- 스레드 시작 
  - start() 메소드 호출  
  - 스레드로 작동 시작  
  - 스레드 객체의 run()이 비로소 실행  
  - JVM에 의해 스케쥴되기 시작함

main 스레드  
- main 스레드  
  - JVM이 응용프로그램을 실행할 때 디폴트로 생성되는 스레드  
    - main() 메소드 실행 시작  
    - main() 메소드가 종료하면 main 스레드 종료  

스레드 종료와 타 스레드 강제 종료  
- 스스로 종료  
  - run() 메소드 리턴  
- 타 스레드에서 강제 종료 

스레드 동기화(Thread Synchronization)  
- 멀티스레드 프로그램 작성시 주의점  
  - 다수의 스레드가 공유 데이터에 동시에 접근하는 경우  
    - 공유 데이터의 값에 예상칯 못한 결과 발생 가능  
- 스레드 동기화  
  - 동기화란?  
    - 스레드 사이의 실행 순서 제어, 공유데이터에 의한 접근이 원활하게 하는 기법  
  - 멀티스레드의 공유 데이터의 동시 접근 문제 해결  
    - 방법1)공유 데이터를 접근하는 모든 스레드의 한 줄 세우기  
    - 방법2)한 스레드가 공유 데이터에 대한 작업을 끝낼 때까지 다른 스레드가 대기하도록 함  
- 자바의 스레드 동기화 방법 - 2가지  
  - synchronized 키워드로 동기화 블록 지정  
  - wait()-notify() 메소드로 스레드의 실행 순서 제어  

synchronized 블록 지정  
- synchronized 키워드  
  - 스레드가 독점적으로 실행해야 하는 부분(동기화 코드)을 표시하는 키워드  
    - 임계 영역(critical section) 표기 키워드  
  - synchronized 블록 지정 방법  
    - 메소드 전체 혹은 코드 블록  
- synchronized 블록이 실행될 때,  
  - 먼저 실행한 스레드가 모니터 소유  
    - 모니터란 해당 객체를 독점적으로 사용할 수 있는 권한  
  - 모니터를 소유한 스레드가 모니터를 내놓을 때까지 다른 스레드 대기  

wait()-notify()를 이용한 스레드 동기화  
- wait()-notify()가 필요한 경우  
  - 공유 데이터로 두 개 이상의 스레드가 데이터를 주고 받을 때  
    - producer-consumer 문제  
- 동기화 메소드  
  - wait() : 다른 스레드가 notify()를 불러줄 때까지 기다린다.  
  - notify() : wait()를 호출하여 대기중인 스레드를 깨운다.  
    - wait(), notify()는 Object의 메소드  
