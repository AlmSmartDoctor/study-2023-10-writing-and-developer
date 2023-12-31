# [4장] 독자 관점에서 릴리스 문서와 장애 보고서 쓰기 (요약).

## 4.1 체인지 로그를 분류, 요약, 종합하는 법.

### 체인지 로그의 양과 만족도의 관계
    - 체인지 로그 양 & 상사/고객 만족도: 너무 많아도, 너무 적어도 안됨.
### 1단계: 선정하기.
    - 독자 1순위.
    - (개인정리) 개발자가 릴리스 노트를 쓸 때, 독자의 입장에서 쓰는 것이 중요.
### 2단계: 분류하기.
    - 리스트들을 개발관점 (새로운 기능 추가, 기능 개선, 오류 수정) / 고객관점 (게임 준비, 게임 중, 게임 종료)으로 분류 가능.
### 3단계: 요약하기.
    - 서술식 -> 개조식 (글을 깔끔하게 만들어주기)
        - Ex: '미리보기에서 텍스트가 잘리는 문제를 해결했습니다.' -> '미리보기 텍스트 잘리는 문제 해결'
### 4단계: 종합하기.
    - "엘리베이터 스피치" 참고.
    - 릴리즈 노트 최상단에 릴리즈 노트 요약을 작성.

## 4.2 고객에게 유용한 정보를 쓰자.

### 개발자 관점과 고객 관점.
    - 체인지 로그는 개발자 관점에서 쓰는 것이 아니라, 고객 관점에서 쓰는 것.
    - 고객 입장에서 해결된 문제를 알려주고, 그 다음에 개발자 입장에서 어떻게 해결했는지 알려주는 것이 좋음.
    - 체인지 로그에 개선내용 & 가치를 알려주는 것이 중요.
        - Ex: '확인/취소 버튼을 누르면 앱이 종료되는 문제를 해결했습니다.' -> '확인/취소 버튼을 눌러도 앱을 종료하지 않고, 다른 작업을 할 수 있습니다.'
### 과거를 리뷰하고 미래를 보여주자.
    - 고객에게 다음 릴리즈에 어떤 기능이 추가될지 알려주는 것이 좋음.
    - 체인지 로그에 TODO도 알려주자.
        - Ex: '건물 가독성 개선 검토'

### Semantic Versioning. (유의적 버전)
    - 체인지 로그의 중요도를 표시하는 방법.
    - Major.Minor.Patch
        - Major: 기존 버전과 호환되지 않는 변경사항.
        - Minor: 기존 버전과 호환되는 변경사항.
        - Patch: 버그 수정.
    - [typescript](https://github.com/microsoft/TypeScript/releases)
    - [nest.js](https://github.com/nestjs/nest/releases)
    - [카카오톡](https://docs.kakaoi.ai/kakao_work/release_note)
    - [create-release](https://github.com/actions/create-release)