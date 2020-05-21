# 스피닝 업 AI
설치 과정은 간단한 데, 파이썬, OpenMPI와 같은 환경을 구축해야한다.

## 개발 환경 구축
### 파이썬
요구 버전 : 3.6 이상

홈페이지에서 받으면 된다. http://www.python.org/downloads

개발자 조쉬 아카임 아저씨는 아나콘다로 설치하길 원하시는데, 필자는 아나콘다 받아서 했다가 환경변수 바뀌고, 파이썬 설치 경로 바껴서, 컴퓨터 고수 서 모씨와 3시간 날려먹은 적 있다. 취향대로 하자.


### PIP 설치
파이썬의 pip가 필요하다. 파이썬이 있는데 pip가 없는 흑우가 있다면 DOS 창을 띄우고 아래와 같이 시도하자.

- PIP 설치
```
 python get-pip.py
```
- PIP 버전 확인
```
 pip --version
```

- PIP 업데이트
```
  python -m pip install --upgrade pip
```

아나콘다를 이용하여 설치하는 방법은 https://spinningup.openai.com/en/latest/user/installation.html#installing-spinning-up 을 참고하자

### OpenMPI<sup id="a1">[1](#b1)</sup>
조쉬 아카임 아저씨는 MS를 혐오하신 나머지, 윈도우즈의 설치 경로를 올려놓지 않으셨다. ~~ 심장이 철렁~ ~~

얘네들은 구버전들은 지원을 안 하기 때문에 최신 버전을 일단 받아보도록 하자.
Version 4.0이 최신 버전이다.

https://www.open-mpi.org/software/ompi/v1.6/ms-windows.php

Windows XP, Windows Vista, Windows Server 2003/2008, Windows 7만 지원하는 플랫폼이라고 적혀 있어, 굉장히 똥줄타게 만드는 프로그램이 아닐까 싶다.


### 스피닝 업 설치
github에 오픈 소스로 올려서 해당 레퍼지토리부터 받아와야 한다. https://github.com/openai/spinningup.git

```
git clone https://github.com/openai/spinningup.git
cd spinningup
pip install -e .
```

### 설치 확인
DOS나 커맨드 창에 아래와 같은 코드를 입력하자.
```
python -m spinup.run ppo --hid "[32,32]" --env LunarLander-v2 --exp_name installtest --gamma 0.999
```
이 코드를 실행하면 10분 정도 걸리는데, ~~ 왜 그걸 이제 말해 ~~ 진정하고 저건 백그라운드에 실행하게 냅두고, 계속 이 문서를 읽어보도록 하자.

저 코드를 실행하면, 학습 진행도를 보게 되는데, 어떤 학습 활동을 하고 있음을 알 수 있다.

트레이닝이 끝나면, 아래 코드를 실행시켜 학습된 비디오를 보자.

```
python -m spinup.run test_policy data/installtest/installtest_s0
```

그리고 다음을 실행시켜보며 마무리하자.

```
python -m spinup.run plot data/installtest/installtest_s0
```
(실행 결과 첨부 예정)
### 참고 사항
스피닝 업을 설치하면 기본적으로 Gym이라는 프로그램이 딸려서 설치되는데, Gym 설치에 문제가 생겼다면 Gym github 페이지에 가서 따지란다.
https://github.com/openai/gym


### 각주
<b id="b1">[1](#a1)</b> Message Passing Interface의 줄임말로, 쓰레드 끼리 메세지 주고 받는 인터페이스를 가르킨다.
