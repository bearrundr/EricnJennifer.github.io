---
layout: post_study
title:  4. 정부3.0 공공 데이터 포털 API 사용하기
date: 2018-01-05 04:01:00
categories: python_crawling
---
## 4. 정부3.0 공공 데이터 포털 API 사용하기
<br/><br/>

2011년 정부는 ‘국가공공데이터포털(http://www.data.go.kr)’이란 국가 공공 정보 사이트를 구축하고 공공 정보 31만 건을 공개한 이후 각 부처가 경쟁적으로 데이터 공개를 시작하였다. 물론, 그 이전에도 데이터를 제공하는 정부 부처가 있었으나 포털(portal)의 형태로 한꺼번에 유관 부처의 공개 데이터를 찾아볼 수 있게 되어 데이터를 공부하거나 상업적으로 사용하는데 편의성을 제공한다.
<br/><br/>
공공 데이터는 특별한 제약 없이 사용할 수 있는데 초기 개발시에는 일일 데이터 조회 제한이 있는 “개발계정”을 활용하다가 서비스가 완성되면 “활용신청”을 통해 데이터 조회 제한 횟수를 증가시킬 수 있다(실제 필자는 활용신청을 해보지 않아 어느 정도까지 되는지는 관련 부처에 문의하기 바란다).
<br/><br/>
<br/><br/>
### 4.1 4.1	공공 데이터 포털 가입
<br/><br/>


공공정보를 활용하기 위해서는 먼저 공공 데이터 포털에 가입을 해야 한다. 포털 페이지(https://www.data.go.kr)를 방문하면 [그림 1]과 같이 각종 관심분야에 해당하는 데이터를 조회하고 다운로드 받을 수 있는 화면이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/31.jpg)
[그림 1] 공공 데이터 포털 초기 페이지
{: .borderBox}
<br/><br/>

페이지 상단의 [회원가입]을 선택하여 [그림 2]와 같은 가입페이지로 이동한다.
<br/><br/>

![](/asset/study/python_crawling/2/32.jpg)
[그림 2] 회원 가입 페이지
{: .borderBox}
<br/><br/>

회원 가입은 “일반회원”과 “기관회원”으로 분리된다. “일반회원” 하단의 “가입하기”를 선택하면 [그림 3]과 같이 회원 가입 여부를 확인하는 창이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/33.jpg)
[그림 3] 회원가입 STEP 1
{: .borderBox}
<br/><br/>

이름과 이메일 주소를 입력하고 [가입 확인] 버튼을 누르면 [그림 4]와 같이 회원 약관 동의 화면이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/34.jpg)
[그림 4] 회원 약관 및 개인정보 수집 동의
{: .borderBox}
<br/><br/>

매번 사이트에 가입을 하면서 느끼는 거지만, 동의하지 않으면 사용할 수 없게 하는 서비스이면서 왜 자꾸 물어보는지 모르겠다. 체크 박스에 동의하고 [동의] 버튼을 누르면 [그림 5]와 같이 가입자 정보를 입력하는 화면이 나온다.
<br/><br/>

![](/asset/study/python_crawling/2/35.jpg)
[그림 5] 가입자 기본 정보 입력
{: .borderBox}
<br/><br/>

가입 등록 항목 중 “인증서 등록” 항목이 있는데 추후 로그인 시 인증서를 사용하고자 하는 경우에 사용할 인증서를 등록할 수 있다. 물론 아마 이 글을 읽는 독자중에 인증서를 등록하는 분은 없으리라 생각한다.
<br/><br/>
이메일을 입력한 후 인증하기 버튼을 누르면 입력한 이메일로 인증코드가 전달된다. 일반적으로 요즘은 이메일과 전화번호 문자메시지 인증을 동시에 하고 있는데, 이메일로만 끝나게 되어 있어서 나름 편안하게 만들어 놓았다.
<br/><br/>
필수 사항(* 표시 항목)을 입력한 후 [완료] 버튼을 누르면 가입이 완료되고 회원 가입이 완료되었다는 화면이 [그림 6]과 같이 회원 가입 완료 페이지가 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/36.jpg)
[그림 6] 회원 가입 완료 페이지
{: .borderBox}
<br/><br/>

이건 개인적인 느낌이지만 공공 데이터 포털의 경우 가입 절차가 이메일 인증 한번으로 끝나게 구성되어 정부에서 제공하는 서비스 포털이 아닌 것 같은 느낌이 든다.
기본적으로 깔아야 하는 프로그램이 수십개에 이르는 포털에 비하면 공공 데이터 포털은 개발자를 위한 사이트여서 그런지, 아니면 공공성을 강조하기 위해서인지 편리함을 느낀다.
[로그인] 버튼을 누르면 [그림 37]과 같이 로그인 화면이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/37.jpg)
[그림 7] 공공 데이터 포털 로그인 화면
{: .borderBox}
<br/><br/>

가입한 아이디와 비밀번호를 입력한 후 [로그인] 버튼을 누르면 비로서 공공 데이터 포털의 데이터를 마음대로 쓸 수 있는 권한을 얻게 된다. [그림 8]은 로그인 후 계정이 활성화 되어 상단에 [마이 페이지]가 나타난 것을 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/38.jpg)
[그림 8] 로그인 후 “마이페이지” 활성화
{: .borderBox}
<br/><br/>

우리는 공공 정보 데이터를 수집하여 Part 4.에서 상관 관계 분석을 해 보려고 한다. 상관분석을 위한 데이터 셋으로 외국인의 입국 숫자에 따른 관광지 입장 수를 사용하려고 한다. [그림 8] 상단에 위치한 검색창에 “출입국 관광 통계 서비스”를 입력한 후 검색하면 [그림 9]와 같이 검색 결과를 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/39.jpg)
[그림 9] 출입국 관광 통계 서비스 검색 결과
{: .borderBox}
<br/><br/>

검색 결과는 크게 3가지 분류로 나타난다. “파일 데이터”는 엑셀, HWP, CVS 등 파일 형식으로 저장되어 있는 데이터로 바로 다운로드 받아서 활용할 수 있다. 파이썬에서 엑셀 파일을 열고, 검색할 수 있으면 편리하게 사용할 수 있는 장점이 있지만, 과거 데이터인 경우가 많아 실시간성을 반영하기는 어렵다.
<br/><br/>
오픈 API는 각 기관의 서버에서 REST API를 이용하여 직접 데이터를 요청하고 수신할 수 있다. 결과값은 XML과 JSON 형태로 제공해 주므로 편리한 형식으로 사용하면 된다. 그러나 실제 오픈 API의 경우에도 실시간성을 반영하기 보다는 제공 기관이 주기별로 업데이트하는 데이터가 제공된다고 볼 수 있다.
<br/><br/>
만약 공공 데이터를 이용하여 웹 서비스등을 사용하려고 한다면 자체 데이터 베이스에 저장을 하고 주기적으로 데이터를 쿼리하거나, 배치 프로그램으로 만들어서 분기별로 데이터를 검색하는 것이 효율적일 것이다.
<br/><br/>
표준데이터는 공공데이터 개발 표준 데이터 속성정보를 따르며, 각 지자체나 단체에서 제공하는 데이터를 표준 형태로 재 가공한 데이터이다. 표준 속성을 따르기 때문에 REST의 End Point만 변경하면서 데이터를 가지고 오면 편리하게 프로그래밍할 수 있는 장점이 있다.
<br/><br/>
“오픈 API” 검색 결과를 선택하면 [그림 10]과 같이 자세한 정보를 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/40.jpg)
[그림 10] 출입국 관광 통계 서비스 활용 신청
{: .borderBox}
<br/><br/>

각 오픈 API는 제공 형식의 아이콘이 있는데 [XML]이라고 표시되어 있는 경우에는 거의 [JSON]형식도 함께 제공하는 것으로 보여진다. 또한 연관 데이터 셋은 자체적으로 지자체에서 제공하는 데이터이다. “출입국관광통계서비스” 우측의 [활용신청] 버튼을 클릭하면 [그림 11]과 같이 개발 계정 신청 창이 나타난다.
<br/><br/>

![](/asset/study/python_crawling/2/41.jpg)
[그림 11] 개발 계정 신청
{: .borderBox}
<br/><br/>

화면의 “기본정보” 사항에 보면 “심의여부”가 “즉시”라고 표기되어 있는 것을 확인할 수 있다. 심의여부가 “즉시”인 경우에는 신청과 동시에 사용이 가능한 데이터이다. 일부 데이터의 경우에는 심사가 필요한 경우가 있고, 관련 서류를 제출해야 하는 경우가 있다.
<br/><br/>
“시스템 유형”은 “일반”과 “서버구축”으로 분리된다. “일반”을 선택하는 경우에는 자체 데이터베이스에 저장을 하지 않는 경우이고 “서버구축”을 선택하는 경우에는 수신한 데이터를 자체 데이터베이스에 저장한다는 것을 의미한다.
<br/><br/>
우리는 출입국 관광 통계를 사용할 예정이므로 맨 하단의 “출입국관광통계”를 선택한 후 “저작권 표시”에 동의한(일반적으로 공공 데이터 포털의 데이터를 서비스에 사용하는 경우에는 자료의 출처를 서비스시에 밝혀야 한다) 후 [신청] 버튼을 누르면 [그림 12]와 같이 바로 승인이 이루어진 것이 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/42.jpg)
[그림 12] 공공 정보 데이터 신청 및 활용 상태 확인
{: .borderBox}
<br/><br/>

만약 심의가 필요한 경우에는 “반려”와 “보류”의 상태를 확인할 수 있으며, 크게 위법의 소지가 없는 경우에는 승인을 해주는 경향이다(실제 승인시 전화 한 통화 정도 하는 경우도 있고 나중에 잘 쓰고 있냐고, 어디에 쓰고 있냐고 물어보는 연락이 오곤 한다).
<br/><br/>
앞에서 “출입국관광통계서비스”와 같은 형식으로 검색 창에서 “관광자원통계서비스”를 검색하여 신청한다. [그림 13]은 두 개의 서비스 신청이 완료된 화면을 나타낸다.
<br/><br/>

![](/asset/study/python_crawling/2/43.jpg)
[그림 13] 개발 계정 확인
{: .borderBox}
<br/><br/>

서비스가 계정이 발급된 항목 중 “관광자원통계서비스”를 클릭하면 [그림 14]와 같이 개발 계정에 대한 접근 “End Point”와 “일일 트래픽” 제한 사항들을 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/44.jpg)
[그림 14] 관광자원통계서비스 개발 계정 상세 정보
{: .borderBox}
<br/><br/>

화면 하단의 [개발 가이드]를 클릭하면 전달 파라미터와 회신 인자에 대한 자세한 매뉴얼을 제공해 준다. 우리는 Part 2. 에서 파이썬을 이용하여 해당 데이터를 가지고 오는 방법에 대해 알아볼 떄 본 자료를 활용할 예정이다.
상단 오른쪽의 [일반 인증키 받기]를 클릭하면 [그림 15]와 같이 키가 발급되고 서비스에 접속할 수 있는 End Point와 키를 확인할 수 있다.
<br/><br/>

![](/asset/study/python_crawling/2/45.jpg)
[그림 15] 일반 인증키의 발급
{: .borderBox}
<br/><br/>

공공 데이터 포털을 관심있게 살펴보면 의외로 웹이나 모바일 서비스로 활용할 수 있는 자료들이 많이 있는 것을 발견할 수 있을 것이다. 검색창을 이용하면 다양한 데이터가 존재하고 있는 것을 확인할 수 있으니, 많이 활용하기를 바란다(실제로 검색을 해보면 파일의 다운로드 수와 활용 신청건수를 확인할 수 있다. 서비스 기획을 할 때 이 숫자를 유심히 관찰해 보는 것도 도움이 될 것 이라 생각된다.)




















