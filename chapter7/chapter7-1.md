## 개발자가 기술 블로그를 잘 못 쓰는 이유

    학생 때 배운 글쓰기 방법은 논설문이나 설명문을 쓰는 방법이기 때문
    1. 이 글을 왜 쓰는가?
    2. 이 글을 읽는 독자는 누구인가?
    3. 이 글을 읽는 독자에게 무엇을 말하려고 하는가?
    4. 이 글이 주장하는 바가 무엇인가?
    5. 이 글이 주장하는 바의 근거가 분명한가?

    => 기술 블로그를 쓸 때 주제가 불분명하고, 독자 수준이 천차만별이고, 딱히 주장할 것이 없다

개발기 -> 그저 개발 과정 그 자체
튜토리얼, 개발 가이드, 개발자 컨퍼런스 후기 -> 그저 방법이나 내용을 전달

기술 블로그에서 주장할 필요도 없고, 주장이 있을 수도 없다. 단지 개발자가 했던 선택과 몇몇 상황에서 더 좋은 방법을 제시할 수 있을 뿐이다.

### 1. 주제 의식을 버리고 소재 의식으로 쓰자
- 민족, 권선징악, 자존감 등 추상적 가치 x
- 특정한 대상이나 상황에 대한 자기만의 관점이나 생각 o
ex) https://techblog.woowahan.com/2607/

### 2. 독자 수준이 아니라 자기 수준으로 쓰자
직장에서 하는 일을 초등학생이 이해할 수 있게 풀어서 쓸 수 있는 사람은 없다.

<details>
<summary>구글 면접관: 8살 조카에게 데이터베이스를 3문장으로 설명해보세요</summary>
비유법은 간접적으로 이해하는 것에 불과하다. 비유법만으로는 초등학생들이 데이터베이스를 한 줄도 만들 수 없다.

= 독자를 만족시킬 수 없으면 그냥 작성자 수준을 쓰는 편이 낫다.
</details>

- 기술 블로그를 쓸 때는 독자를 생각해서 어려운 용어를 일부러 해석하거나 쉬운 용어로 바꿀 필요가 없다.
- 중요한 건 핵심 내용만 쓰고 나머지는 독자가 공부할 수 있게 길만 터놓는 것

### 3. 재미있게 글을 쓰자
자신의 경험을 녹여내거나 기교를 부리지 않음 = 정확하고 군더더기 없이 깔끔, 대신에 재미가 없다

ex) https://ko.wikipedia.org/wiki/%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D

ex2) https://namu.wiki/w/%EA%B0%9D%EC%B2%B4%20%EC%A7%80%ED%96%A5%20%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D

## 글의 종류별로 목차 잡는 법 1 - 저술

### 기술 블로그의 4종류 - 저, 술, 편, 집
- 저 = 직접 경험하고 실험한 과정이나 결과
- 술 = 어떤 것을 분석하여 의미를 풀이하고 해석한 것
- 편 = 산만하고 복잡한 자료를 편집해 질서를 부여한 것
- 집 = 여러 사람의 견해나 흩어진 자료를 한데 모아 정리한 것

### 저 (개발기, 도입기, 적용기)
\* 목차를 잘 잡아서 본문부터 쓰자

- 목차는 성공한 루트와 실패한 루트를 구분해서
- 머리말은 처음부터 쓰기에 어려우니 \
 본문부터 쓰고, 맺음말로 정리하고, 마지막에 글을 올릴 때 생각나는 대로 간략히 머리말 작성

### 술 (기술 소개, 용어 분석, 에러 해결 방법)
\* 원전을 비교하고 실험해 풀이해서 쓰자

ex) GET과 POST의 차이
원전: HTTP/1.1 프로토콜 https://datatracker.ietf.org/doc/html/rfc2616

원전은 그저 Method를 나열하고 있다. \
이걸 읽기에는 힘드니까 GET과 POST의 설명을 토대로 두 메소드를 비교하면 자연스럽게 글을 쓸 수 있음
https://hongsii.github.io/2017/08/02/what-is-the-difference-get-and-post/

이런 거 뿐만 아니라 서비스 성능을 높이기 위해 직접 여러 실험을 해보고 결과를 잘 정리하기만 해도 좋은 글이 된다.
https://tech.kakao.com/2018/06/19/mysql-ascending-index-vs-descending-index/