# 1. 서비스 개념을 범주, 용도, 특징으로 설명하자

```
범주 : Amazon Simple Storage Service(Amazon S3)는 인터넷 스토리지 서비스입니다
용도 : Amazon S3를 사용하면 인터넷을 통해 언제 어디서든 원하는 양의 데이터를 저장하고 검색할 수 있습니다.
특징 : AWS Management Console의 간단하고 직관적인 웹 인터페이스를 통해 이러한 작업을 수행할 수 있습니다.
```

## 1.1. 범주를 정확하게 선택하자

- AWS는 Amazon S3의 범주를 독자에게 익숙한 인터넷 스토리지 서비스로 정의
  - 독자는 이미 알고 있는 인터넷 스토리지 서비스의 범주에서 Amazon S3를 추가하기만 하면 됨
- 산업이나 서비스의 범주를 사용할 때 주의할 점
  - 유사한 용어를 여러 개 사용
  - 인터넷 스토리지 서비스 : 웹하드 서비스, 웹 스토리지 서비스, 파일 호스팅 서비스, 온라인 스토리지 서비스 등으로 불리다 현재는 클라우드 스토리지 서비스로 불림
  - 그러나 서비스 방식이 조금씩 다름

## 1.2. 용도를 범주의 핵심 기능으로 기술하자

Amazon S3를 사용하면 인터넷을 통해 언제 어디서든 원하는 양의 데이터를 저장하고 검색할 수 있습니다.

> 서비스의 핵심 기능 = 서비스가 속한 범주의 핵심 기능

## 1.3. 특징을 장점과 강점에서 뽑아 쓰자

| 구분   | A사 | B사 | C사 |
| ------ | --- | --- | --- |
| 기능 a | 5   | 1   | 3   |
| 기능 b | 1   | 3   | 1   |
| 기능 c | 3   | 4   | 5   |

- 장점은 자기 기준
  - B사의 장점 = 기능 c
- 강점은 비교 우위
  - B사의 강점 = 기능 b

# 2. 정확히 이해하도록 그림과 글로 묘사하자

## 객관적 묘사와 주관적 묘사 둘 다 하자

- 주관적 묘사
  - 저기 앞에 큰 사거리에서 오른쪽으로 돌아서 5분쯤 가면 기차역이 보여요
- 객관적 묘사
  - 두 번째 사거리에서 10시 방향으로 돌아서 300미터 가면 우측에 기차역이 있어요

```
안녕하세요. 기획팀입니다. 고객과 좀 더 소통하기 위해 홈페이지 라이브 채팅 기능을 추가하려고 합니다. 경쟁사 홈페이지의 해당 기능과 비슷하게 만들면 됩니다. 홈페이지 우측 하단에 위치하되 원래 텍스트를 가리지 않아야 합니다. 크기는 우리가 쓰는 메신저만하면 좋겠는데 필요 시 크기 조절이 가능했으면 좋겠습니다. 그 외 특별한 요청은 없습니다. 다음 주까지 완료될까요?
```

\[ 요구사항 \]

- 기존 홈페이지에 라이브 채팅 기능 추가
- 채팅창은 홈페이지 우측 하단에 위치
- 채팅창이 원래 텍스트를 가리지 않게 하기
- 메신저 크기지만 크기 조절가능
- 다음 주까지 완료

\[ 질의 내용 \]

.

.

.

```
요구명 : 채팅창 크기
요구ID : C001-1
요구내용 : 채팅창 크기는 화면에 디스플레이된 페이지 크기에서 가로 20%, 세로 25%로 정한다. 채팅창의 최소 크기는 가로 150px, 세로 200로 한다. 디스플레이된 페이지 크기가 가로 756px 이하, 또는 세로 600px 이하일 경우에는 채팅창을 가로 50px, 세로 50px의 아이콘 이미지로 자동으로 대체되게 한다. 아이콘 이미지를 클릭하면 새 창에서 채팅창을 단독으로 디스플레이 한다.
```
