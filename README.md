
알뜰 서울의 발견 (Finding of AlDdle Seoul)
===============

서울시 홈페이지는 1000만개!! 무슨 소리냐구요? 생계, 주거, 복지, 문화 뭐 서울시가 제공하는 서비스는 여기저기 수없이 많은데, 우린 항상 바쁘죠. 정신차려보면 다 지나갔더라고요. 바로 시민이 자신의 다양한 조건(나이, 성별, 가족, 사는 곳, 직업)을 넣으면 그 조건에 맞는 서울시의 서비스를 보여주고 활용할 수 있게 하는 겁니다. 지금은 발품팔고 뛰어다녀도 찾기 힘든 시절이잖아요. ^^

- 서울시에서 제공하는 혜택을 나에게 맞춰 필터링하는 서비스.
- 서울시가 제공하는 혜택에 대한 시민들 평점 서비스.
- 서울시에서 제공하는 혜택을 제대로 파악하여 내가 낸 세금 이상으로 행정서비스를 활용해 보자.

이런 거 어떤가요? 같이 만들어갈 수 있습니다!

## 서비스 개요

야심차게 시작했으나 리서치하고 정보를 취합해보니 압도될 정도의 방대함을 자랑하시어, 이대로 가다가는 노가다만 하다가 잘 진전이 안되겠다 싶었고, 서울시나 복지부 등에서 이미 비슷한 서비스를 제공하고 있어서 좀 위축됐지만 그래도 여전히 개선할 부분이 많다고 생각해서 다시 함께 힘을 내고 있나요?

## 개발 환경

현재 팀원들과 앞으로의 참여자들간의 새로운 기술 경험, 공부 및 공동 개발을 위해 오픈소스 nodejs 프레임워크를 선택했습니다. 또한 사용성을 높이기 위해서 앱을 사용하고 스트림 형태로 제공하고 위해 mongodb를 선택했습니다.(아 이거랑은 상관없나요? 그냥 했습니다. :) 클라이언트는 웹사이트, 안드로이드앱 정도로 기획 중입니다. 음 일단 총대를 맨거라 프레임워크가 변경될 수도... ㅡ,.ㅡ;;;

### Loopback
nodejs MBASS(Mobile Backend as s Service framework)
http://loopback.io

### Mongodb
Document 기반의 NoSQL 스토리지
http://mongodb.org

### Vagrant [|veɪgrənt]

Vagrant는 ruby로 작성한 개발 환경 구축을 위한 도구로써, 개발 환경 구축하는데 드는 시간을 줄일 수 있으며 각각 다른 OS나 환경의 개발자들이 동일한 개발 환경에서 협업할 수 있습니다.

가장 큰 특징은 게스트 OS (vagrant가 제어하는 가상머신)의 자원을 활용하면서 개발자가 사용하는 머신의 호스트 OS에서 소스를 편집할 수 있다는 점입니다. 호스트 OS의 디렉토리를 게스트 OS에 마운트시키고 그 소스를 게스트 OS에서 돌리는 겁니다. 예를 들면 윈도우나 맥을 사용하는 개발자가 리눅스 기반의 환경에서 돌아가는 프로젝트를 이미 사용 중인 개발도구나 소스 편집기를 활용해서 개발할 수 있다는 거죠~

### 사용방법

####1. 소프트웨어 설치

- Virtualbox (http://virtualbox.org)
- Vagrant (http://vagrantup.com)

####2. 가상머신 시작

```
git clone https://github.com/codeforseoul/nogo_workingmon.git
cd nogo_workingmom/
git checkout setup
vagrant up

```
좋아하는 음료수를 마시거나 담배 한 대 태우시거나 산책을 하고 돌아오면 개발 환경 완성!

####3. 프로젝트 시작

```

// ubuntu trusty32 가상머신으로 로그인
vagrant ssh

// 기본적으로 vagrant는 호스트 OS의 현재 디렉토리를 게스트 OS의 /vagrant로 마운트합니다.
cd /vagrant/nogo_workingmom/server

// 필요한 node 모듈을 설치합니다.
npm install

// 프로젝트 띄우기
slc run

```
브라우저에서 http://0.0.0.0:3000/explorer 로 접근하면 api를 테스트해볼 수 있습니다.

####4. 불타는 코딩!
아주 작은 커밋이 모여 바다가 됩니다. 불살라주세요~ ㅋㅋㅋㅋ 아님 이슈라도 달아주심 감사~

####5. 두근두근 pull request!
창피해하지 마세요. 여러분이 더 대단합니다. 아마도, 당연히, 격하게 환영합니다!


### 구조

#### 사용자

- username
- password
- email
- signed_in
- logged_in
- gender // 성별
- age // 나이
- regions // 지역
- interests // 관심사
- twitter
- facebook

#### 서비스
- id
- title
- url
- body
- author
- image
- interests

###

