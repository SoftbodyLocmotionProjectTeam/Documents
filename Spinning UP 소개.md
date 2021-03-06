# 스피닝 업

강화학습 교육용으로 만들어진, 오픈 API. [딥 강화 학습]<sup id="a1">[1](#b1)</sup>을 배우는 데 좋다.
#### 
## 소개
버클리 공대의 딥 강화 학습 연구원 **조시 아키암** 아저씨가 강화 학습에 친숙하지 않은 사용자들을 위해서, 컴퓨터에게 시행착오를 통해 문제를 해결하도록 머신 러닝 접근법을 제공한다.  
####
## 홈페이지
홈페이지에서는 다음과 같은 내용을 제공한다.
https://spinningup.openai.com/en/latest/user/introduction.html
 - 강화 학습 관련 용어, 알고리즘, 이론에 대해 짧은 설명 
 - 강화 학습으로 어떻게 연구를 키울지 짧은 에세이
 - 중요 논문들을 주제로 묶어서 선별한 리스트
 - 핵심 알고리즘의 git 레퍼지토리
 - 연습용 예제
####
## 스피닝 업 AI를 만든 이유

AI 안정성에 기여하기 위해서란다. ~미리미리 스카이넷 코인 탑승하시는 것 같다.~
여기서, 딥러닝과 딥 강화 러닝에 아주 차이를 두고 있는데, 인간들이 딥 러닝까지는 아주 쉽게 발전시켰는데, 딥 강화 러닝은 빡세다고 한다. 만드신 분은 딥 러닝도 버거운 학생들에게 딥 강화 러닝을 하이 레벨 언어로 다루게 해주는 은혜를 하사하시겠단다.
 
 ####
그런데, 함정이 있다. 하이레벨로 올라가다 보니, 새로운 함수, 변수 따위의 필드 정의가 필요했고, 이걸 쓰는 사람들에게 하이레벨에서 좋아하는 앱스트렉션(추상화)을 설명해줘야 한다. 따라서, 이것을 잘 한다고 딥 강화 학습을 잘하는 것이 아니고 그냥 스피닝 업 API를 잘 쓰는 것이다. 조쉬 아키암은 그래도 맛배기로 딥 강화 학습을 조금 다뤄보면서 조금이나마 이해할 것이라고 말씀하셨다.

딥 강화 러닝에 흥미가 있는 사람에게 누락된 중간 단계를 제공한다며 우리같은 초심자 뿐만 아니라 전문가들에게도 AI 세이프티 문제를 다룰 수 있게 도와준단다. 오픈 소스로 제공하시는 것 보니 선량한 아재로 보인다.

####
## 오픈 AI
오픈 API가 아닌 AI다. 헷갈리지 않도록 주의하자.
[AGI]<sup id="a2">[2](#b2)</sup>에게 안정적인 개발환경을 주고 싶은 것이 이 오픈 AI의 목적이다. 이 AI를 이용하면, 인공 지능 개발을 보다 안정적이고 확실하게 할 수 있다고 한다. 조쉬 아키암은 이게 널리 퍼져서 이것이 발전됬으면 좋겠다고 오픈 소스로 공개하였다.
####

## 코드 설계 철학
스피닝 업을 만들 때 다음과 같은 철학을 지키셨다고 한다.
- 우수함을 유지하면서 가능한 아주 간단하게 만들자
- 일관성 있게 코딩해서 근본적으로 비슷한 알고리즘들은 그대로 보여주자. 
(원문은 highly-consistent with each other to expose fundamental similarities between algorithms. 인데 무슨 소리인지 도통 모르겠어서 뇌피셜로 적었다. 이해되는 사람이 적자.)

####

요약하면, 딥알못들이 이해하기 쉽게 만들었다는 소리다. 코드 이해하려고, 깊게 파고 들거나, 이 참조 저 참조 따라다니지 않게 만들었다는 소리다. 물론 로그 찍는 거나 저장, 불러오기, [MPI][AGI]<sup id="a3">[3](#b3)</sup> 이런 것은 더럽게 되있다고 시인했다. 

####

알고리즘에서 쓰는 트릭을 최소화 했다고 한다. 그리고 알고리즘들을 엥간해서는 다 통일했다고 한다. 가령, 소트는 무조건 힙소트로 통일한다던지, 탐색 방법을 DFS만 쓴다던지 하신 것 같다. 

####

## 프로젝트 타임 라인
우리 프로젝트에서는 무쓸모이므로 생략한다.

####

 ## 용어 설명
 <b id="b1">[1](#a1)</b> 딥러닝과 강화 학습을 합친 말이다.
 
 <b id="b2">[2](#a2)</b> Aritificial General Intelligence의 줄임말로, 범용 인공지능이다.
 
 <b id="b3">[3](#a3)</b> Message Passing Interface의 줄임말로, 쓰레드 끼리 메세지 주고 받는 인터페이스를 가르킨다.
 
 
