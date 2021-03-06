---
layout: post_study
title:  시작하기 - PYTHON 설치
date: 2017-12-28 01:01:00
categories: python_basic
---

파이썬(Python)은 프로그래머인 귀도 반 로섬(Guido van Rossum)이 1991년도에 발표한 프로그래밍 언어로, 플랫폼 독립적이며 인터프리터(Interpreter)식, 객체지향적(object oriented), 동적 타이핑(dynamically typed) 대화형 언어이다. 파이썬이라는 이름은 귀도가 좋아하는 코미디 〈Monty Python's Flying Circus: 몬티 파이썬의 날으는 써커스〉에서 따온 것이라고 한다. 파이썬은 고대 그리스 신화에 나오는 큰 뱀을 의미하며, 이 때문에 파이썬의 로고로 뱀 모양을 사용하고 있다.
<br />
<br />
파이썬은 비영리로 운영되는 ‘파이썬 소프트웨어 재단’이 관리하는 개방형, 공동체 기반 개발 모델을 가지고 있으며 무료로 누구나 다운로드 받아 사용 가능하다.
<br />
<br />
파이썬을 다운로드 받기 위하여 공식 홈페이지인 https://www.python.org 로 이동하면 [그림 1]과 같이 메인 홈페이지를 만날 수 있다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/1.png)
[그림 1] 파이썬 메인 홈페이지
{: .borderBox}
<br />
<br />
파이썬 메인 홈페이지의 [Downloads]메뉴를 클릭하면 [그림 2]와 같은 화면이 나타난다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/2.png)
[그림 2] 파이썬 다운로드 메뉴
{: .borderBox}
<br />

2017년 6월 10일 현재 파이썬은 3.6.1 버전과 2.7.13 버전이 출시되어 있다. 일반적으로 프로그래밍언어는 하나의 형태가 계속 버전업 되는 형태인데 파이썬의 경우에는 2.X 와 3.X 버전이 있다. 3.X 버전에서는 모든 변수가 객체의 형식으로 처리된다는 점과 유니코드(Unicode)를 지원하는 것이 2.X 와의 차이라고 할 수 있다(2.X 와 3.X는 지원하는 모듈과 문법적인 변경이 있으므로 주의하여야 한다). 
공식적으로 파이썬 2.X 버전은 2.7.X 버전을 기준으로 제품의 개발이 종료되었으며, 3.X 버전이 계속 업데이트 되고 있는 상황이므로 모든 코드는 3.X를 기준으로 설명한다.
<br />
<br />
[그림 2]의 [All Releases]를 선택하면 현재까지 릴리즈된 모든 버전을 확인할 수 있다. 본 과정에서는 파이썬 3.5.1을 기준으로 사용하였으므로 [그림 3]에서 3.5.1 버전을 찾아 다운로드를 클릭한다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/3.png)
[그림 3] 파이썬 다운로드(모든 버전중 3.5.1 선택)
{: .borderBox}
<br />
<br />
3.5.1 버전을 선택하여 [Download]를 클릭하면 [그림 4]와 같이 파이썬 3.5.1 버전의 특성 및 다운로드 페이지가 나타난다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/4.png)
[그림 4] OS 별 설치 파일 선택 및 다운로드
{: .borderBox}
<br />

자신이 사용하는 OS의 버전 및 프로세서 종류에 맞는 파일을 선택한 후 다운로드 하여 PC에 저장한다(본 과정에서는 마이크로소프트 윈도우 운영체제를 기본으로 한다).
<br />

![파이썬 설치](/asset/study/python_basic/1/5.png)
[그림 5] 파이썬 3.5.1 설치 파일
{: .borderBox}
<br />

[그림 5]와 같이 탐색기에서 다운로드 받은 디렉터리로 이동하여 실행파일을 실행시키면 [그림 6]과 같이 설치화면이 나타난다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/6.png)
[그림 6] 파이썬 설치 1
{: .borderBox}
<br />

파이썬 설치 파일은 기본설정으로 설치하기 위한(Install Now)와 사용자 설치(Customize installation)를 지원한다. ‘Add Python 3.5 to PATH’ 항목에 체크를 하면 윈도우 경로(PATH) 파일에 파이썬 설치 디렉터리를 추가하여 도스창(Windows Command)의 어느 경로에서든 파이썬을 실행할 수 있도록 지원한다. 해당 항목에 체크(PATH를 추가하지 않는 경우에는 파이썬 기능을 사용하기 위하여 해당 패스로 항상 이동해야 하는 번거로움이 발생할 수 있다)를 한 후 [Customize instllation]을 클릭하면 [그림 7]과 같은 창이 나타난다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/7.png)
[그림 7] 파이썬 개발환경 옵션 선택
{: .borderBox}
<br />

[그림 7]은 파이썬 기본 프로그램에 추가적으로 설치가 가능한 옵션을 선택하는 창이다. 선택할 수 있는 옵션의 각 기능은 다음과 같다.
<br />

| 항목 | 내용 |
| -------- | -------- |
|   Documentation     |   파이썬 관련 문서 설치     |
|pip	|파이썬 추가 패키지(라이브러리)를 손쉽게 설치할 수 있도록 지원|
|tcl/tk and IDLE|	파이썬 GUI(Graphic User Interface) 표준 라이브러리인 Tkinter의 설치 및  파이썬 통합개발환경(IDLE: Integrated DeveLopment Environment) 설치|
|Python test suite|	파이썬 단위 모듈 테스트를 지원하는 프레임워크(Framework)|
{: .table table-striped}

<br />
필요한 기능을 선택한 후 (pip 와 IDLE는 필수적으로 선택하는 것이 정신건강에 좋다) [Next]버튼을 누르면 [그림 8]과 같이 추가 옵션을 선택하는 창이 나타난다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/8.png)
[그림 8] 파이썬 설치 추가 옵션
{: .borderBox}
<br />

필요한 추가 옵션을 선택한 후 설치 경로를 지정한 후 [Install] 버튼을 누르면 [그림 9]와 같이 설치가 진행된다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/9.png)
[그림 9] 파이썬의 설치
{: .borderBox}
<br />

설치가 완료되면 [그림 10]과 같이 완료 메시지가 나타난다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/10.png)
[그림 10] 파이썬 설치 완료
{: .borderBox}
<br />

[그림 10]과 같이 설치가 완료되었으면 [그림 11]과 같이 [시작]  [모든 프로그램]  [Python 3.5] 메뉴가 생성되고 지정한 파일이 생성된 것을 확인할 수 있다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/11.png)
[그림 11] Python 3.5 메뉴
{: .borderBox}
<br />

설치가 완료되었으면 ‘Python 3.5(64-bit)’ 또는 ‘IDLE(Python 3.5 64-bit)’를 선택하여 파이썬 개발환경을 실행시킬 수 있다. [그림 12]는 ‘Python 3.5(64-bit)’를 실행시킨 것이며 [그림 13]은 ‘IDLE(Python 3.5 64-bit)’를 실행시킨 것이다. IDLE를 사용하게 되는 경우에는 프로그램 파일의 저장, 불러오기 등의 통합환경을 제공하므로 훨씬 편하게 사용할 수 있다.
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/12.png)
[그림 12] Python 3.5 인터프리터(쉘) 실행
{: .borderBox}
<br />
<br />

![파이썬 설치](/asset/study/python_basic/1/13.png)
[그림 13] Python IDLE 인터프리터(쉘) 실행
{: .borderBox}
<br />

인터프리터는 파이썬 쉘(Python Shell)이라고 하며, ‘>>>’는 프롬프트(prompt)라고 한다. 이로써 파이썬 개발 환경의 설치가 마무리 되었다.
