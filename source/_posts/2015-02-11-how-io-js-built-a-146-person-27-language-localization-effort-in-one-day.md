---
category: articles
title: 겨우 하루 만에... io.js는 어떻게 146명이 참가하는 27개 언어 지역화라는 성과를 냈는가
author: mikeal
ref: How io.js built a 146 person, 27 language localization effort… in one day.
refurl: https://medium.com/@mikeal/how-io-js-built-a-146-person-27-language-localization-effort-in-one-day-65e5b1c49a62
translator:
  - <a href="https://github.com/xarus01" target="_blank">Taegun Park</a>
---

커뮤니티에 참여를 요청한다면 그들은 기꺼이 도와줄 것입니다.

나의 첫 한국 방문에서 나는 그곳에 거대한 Node 커뮤니티가 있을 뿐만 아니라, 우리가 생각지도 못했던 그들의 지원 네트워크와 자료들을 가지고 있다는데 깜짝 놀랐다.
현재까지는, 이것이 바로 복수의 언어가 사용되는 큰 커뮤니티들이 그들의 지역 커뮤니티를 지원하고 또 기능해온 방식이었다.

![@isaacs, @mikeal 그리고 play(node) 관계자들, 2012년 가을, 대한민국 서울.](https://d262ilb51hltx0.cloudfront.net/max/676/1*dgwsAsTXAJsvYBOdo1KZaw.png)

@isaacs, @mikeal 그리고 play(node) 관계자들, 2012년 가을, 대한민국 서울.

io.js의 비전 중 하나는 커뮤니티가 이 프로젝트의 모든 면에 참여하고 추진하며, 이러한 커뮤니티에 의해 io.js가 발전하고 성장하는 것이다. 나는 지역화를 할 때가 되었을 때 단순히 웹 사이트나 문서를 번역하는 그룹을 만들고 싶지 않았다.

그 대신 나는 다양한 언어를 사용하는 커뮤니티 구성원들이 모여 자신들의 언어로 협력할 수 있는 공간을 만들고 싶었다. 구성원들은 그 공간을 문서를 번역할 때는 물론 지역 커뮤니티를 지원하고 지역 커뮤니티와 io.js 프로젝트를 연결하는 가교 구실을 할 때도 사용할 수 있다. io.js에서 개방 협력 체제를 통해 에반젤리즘, 소셜 미디어, 심지어 프로젝트의 로드맵까지 만들어 낸 바 있다. 비영어권 커뮤니티라고 여기에 참여하지 못할 이유가 있을까?


# 놀라웠던 토요일!

우리의 웹 사이트 프로젝트 내에는 웹사이트와 과거의 블로그 글을 스페인어로 번역하는 사람들이 몇 있다.
NodeSchool에서 시작된 작업을 준비하면서 그들에게 혹시 결과물을 정리하기 위한 스페인어 지역화 저장소/팀이 필요한지 물어보았다.

![대만 NodeSchool](https://d262ilb51hltx0.cloudfront.net/max/591/1*TBi0lYS4iYoGMQsXvRB4vw.png)

대만 NodeSchool

나는 웹사이트 저장소에 혹시 지역화 작업에 참여하고 싶은 사람이 있는지 묻는 [이슈](https://github.com/nodejs/website/issues/125)를 생성했다. 트위터에서 몇몇에게 링크를 알려주었고 곧 엄청난 수의 사람들의 참가 신청을 볼 수 있었다.

이슈에 코멘트를 남김으로써 참가를 신청한 모든 사람들은 각자의 언어에 해당하는 팀에 배정되었다. 이 팀은 그들의 언어에 해당하는 iojs Github 단체 저장소의 관리자이다. 각 저장소를 설정한 후에 몇 가지 "first step"을 알리는 이슈를 생성했다. 사람들이 이런 새로운 장소를 그들이 완전히 소유한다고 느끼게 만드는 것은 어려움이 따른다. 의도적으로, 각 저장소의 설명과 README 파일을 빈 채로 놓아두었는데 그로 하여금 각 언어 사용자들의 첫 번째 일거리가 그들의 언어로 이것들을 작성하는 것이 되게 하기 위해서였다.

나는 또 그들에게 지역화 팀에서 사용하게 될 트위터 계정과 지역 커뮤니티에서 접근하기 용이한 다른 소셜 미디어 계정을 만들도록 했다. io.js는 소셜 미디어를 통해서 기여자들을 불러모으고 중요한 안건들에 대한 주의를 끄는데 있어 많은 성과를 거두고 있었으며 또한 소셜 미디어를 통해서 우리가 이루어 낸 성과들을 말함으로써 사람들에게 의욕을 주고 신나게 해 왔다. 소셜 미디어 계정을 만듦으로써 성취하고자 한 목표는 이러한 성공들을  재현하고, 그럼으로써 이 팀들의 영역을 "번역자"에서 "커뮤니티 관리자"로 확대하는데 있었다.

마지막 단계로써 나는 이 팀들이 [최신의 주간 io.js 업데이트](https://medium.com/node-js-javascript/io-js-week-of-february-6th-2015-e185388549a4)를 번역하는 작업을 새로운 이슈로 생성하도록 권했다. 이것은 각 그룹이 어떻게 작업을 정의하고 나눌것인지 고민하도록 하는 교묘한 장치였다. 몇몇 속도가 빠른 커뮤니티들은 두사람 이상이 동시에 동일한 글을 번역하는것과 같은  혼란에 빠지기도 했다. 물론 이러한 문제들은 금세 해결되었고 그들이 스스로 과정들과 그에 수반되는 절차들을 만들어냈기 때문에 그들 스스로가 대단한 주인의식을 가지게 되었다. 만약 나나 다른 사람들이 과정들을 알려주고 따르도록 했다면 그렇지 못했을것이다.

진짜 재미있는것은 사람들에게 어떠한 안내도 하지 않은 채로 어떠한 일들을 하는 지 관찰하는 것이었다. 하루가 채 끝나기도 전에 사람들은 웹사이트를 번역하고, 팀원들을 추가하고, 공용 이메일을 만들고, 계정 정보를 팀 내에서 공유하기 위한 다양한 방법들을 고안해냈다.

![최초의 물속 JS 강연! JSConf.asia 2013, 필리핀](https://d262ilb51hltx0.cloudfront.net/max/1400/1*sfXB3BWvgQEmzEEw8Y_sjg.png)

최초의 물속 JS 강연! JSConf.asia 2013, 필리핀


## 언어 vs 지역화

사람들은 빠르게 팀이 언어 당 생성되며 지역마다 할당되는것이 아님을 눈치챘다.(es는 생성되지만 es_ES는 아닌것처럼) 이 팀/저장소들은 각각이 협업이 실제로 일어나는 장소이며 나는 구성원들이 참여하고 서로를 이해할 수 있는 가능한 큰 집단을 만들기를 바랬다. 예를 들어서, 스페인어 팀(iojs-es)은 서로 다른 지역화의 결과물들을 만들어내기 위해(es_ES, es_MX, es_CO 등등의) 서로 쉽게 소통하고 효과적으로 협업할 수 있다. 그들은 또한 행사에 참여 가능한 연사들의 목록을 서로 공유함으로써 우리의 국제적인 에반젤리즘 성과를 키워나가는데 기여할 수 있다.

# 네트워크의 효과

나는 하루의 상당부분을 Github 관리자 도구를 사용하는데 사용했다: 팀을 만들고, 멤버들을 추가하고, 저장소를 만들고, 이슈를 생성하는데.

새로운 사람들이 속속 참가신청을 했다. 맨 처음에는 트위터에서 이것에 대해서 알게 된 사람들이 그들의 친구들에게 알려주었고, 그들 중 얼마가 참가신청을 했을것이다. 각각의 지역화 팀이 첫 번째 이슈에 있는 과정들을 따라가며 일하기 시작했을때 그들은 팀의 트위터 계정을 생성하고, @official_iojs를 팔로우했다. 그리고 @official_iojs가 참가자들에게 각각의 지역화 팀의 트위터 계정을 팔로우하도록 알리는 트윗을 작성했다. 각각의 새로운 지역화 팀 계정을 알리는 트윗들은 리트윗되고 순환하며, 또 다른 참가 신청의 파도를 불러왔다.

위와 같은 일이 매 시간마다 각각의 시간대에서 일어났으며 한 시간마다 몇 개의 새로운 언어가 지역화 작업에 추가되는 결과를 만들어냈다. 일요일 아침(태평양 표준시)에 일어나서 잠든 동안 참가 신청을 한 사람들을 모두 추가했다. 그리고 하루 동안 얼마나 사람들이 모였는지를 확인하고는 27개 언어를 사용하는 146명의 사람들이 단 하루 만에 모여들었다는데 경악을 금치 못했다.

만약 우리가 이 모든 것을 하루 만에 성취할 수 있었다면, 한 달 후에는 어떤 놀라운 일들이 벌어질 수 있을지 몹시 기대된다 ☺
