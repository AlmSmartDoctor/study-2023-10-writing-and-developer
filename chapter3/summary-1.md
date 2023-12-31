# 사용자와 소통하는 에러 메시지 쓰기 1

## 에러 메시지를 쓰기 전에 에러부터 없애자

#### 웹사이트를 탐방해보자 (404에러가 나고 있는 곳을 찾아보자!)

1. [구글의 404](https://www.google.com/404)
   - 404 에러네? 페이지를 찾을 수 없어. 우리가 아는 것은 그게 다야
2. [위키피디아의 404](https://en.wikipedia.org/404)
   - 해당 페이지를 찾을 수 없음을 알려준다.
   - 사용자의 행동을 기반으로 URL을 추측해서 제안한다.
   - 추측된 URL -> 404에러에 대한 내용
3. [yes24의 404](https://www.yes24.com/404)
   - 그나마 꽤 친절한 편이다.
4. [네이버의 404](https://www.naver.com/404)
   - 네이버의 404도 yes24와 비슷하다.
5. [캐시닥 병원이벤트의 404](https://user.yeogiya.io/404)
   - 심플 그 자체

#### 사용자가 404에러를 맞닥뜨리게 되는 상황은 어떤 상황인가?

1. 사용자가 **URL을 잘못 입력**한 경우 -> 사용자 책임
2. 사용자가 **링크를 클릭했으나 해당 페이지가 없는 경우** -> 개발자 책임이다. 이것을 죽은 링크, 혹은 깨진 링크라고 부른다.

#### 어떻게 하면 깨진 링크를 찾을 수 있을까?

- https://www.brokenlinkcheck.com

#### 개발자용 에러 메시지와 사용자용 에러 메시지를 분리하자

## 사용자 에러 메시지를 제대로 쓰는 법

- 에러 메시지에는 에러 내용, 에러의 원인, 에러 해결 방법. 이렇게 3가지가 작성되어야 한다.
  - (예시: 휴대폰 번호를 잘못 입력하셔서 회원가입을 진행할 수 없습니다. 휴대폰 번호 입력란에는 숫자만 입력하십시오.)

#### 에러 메시지를 보여주는 순서

- **만약에 이런 메시지라면 뭐라고 해야 될까?**
  - [에러 내용] 요청한 아이템의 인계를 시간 내에 처리하지 못함
  - [에러 원인] 아이템을 인계받을 상대방에게 다른 사용자가 아이템을 인계하는 중이어서 동시에 인계할 수 없었음
  - [에러 해결 방법] 3초 후에 다시 시도
- 이 때는 해결방법을 먼저 설명하고, 내용이나 원인을 간략하게 설명하는 방법으로 가자 (예시: 3초 후에 다시 시도하십시오. 상대방이 다른 사용자의 아이템을 인계받는 중입니다.)

#### 메시지를 오락가락하게 작성하지 말자. 사용자가 착각할 만한 메시지가 아니라 확실하게 알아들을 수 있어야 한다.

**예시**

- (BAD) 지금 이 페이지를 떠나면 편집한 내용이 취소될 수도 있습니다. 취소하시겠습니까?
- (GOOD) 편집한 내용을 삭제하고 다른 페이지로 이동하시겠습니까?

#### 버튼의 경우 단순히 '예/아니오'로 하기보다는 특정한 행동을 유도할 수 있도록 하자.

- (예시) 페이스북의 경우 '이 페이지에 머물기/페이지에서 나가기'
- (예시) '삭제하고 이동하기/계속 편집하기'
