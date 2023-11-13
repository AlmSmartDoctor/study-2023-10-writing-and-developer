# 개발 시간을 줄여주는 이름 짓기와 주석 쓰기

## 03 좋은 이름의 기준, SMART

### Searchable
- 이름 자체에 범주를 담아둔다.
- 같은 접두어를 가진 함수나 변수가 너무 많으면 이를 적절히 분류한다.
``` yaml
# 안 좋은 예
SERVER_TIMEOUT
NO_RESULT
BAD_REQUEST
SERVER_ALLOWED_REQUESTS_EXCESS
```
``` yaml
# 좋은 예
ERROR_SERVER_TIMEOUT
ERROR_NO_RESULT
ERROR_BAD_REQUEST
ERROR_SERVER_ALLOWED_REQUESTS_EXCESS
userBuyer
usertPayer
userRegister
userRegisterButNoPayer
```

### Mixable
- 개발 언어의 문법과 조합해 이름을 짓는 것이 좋다.
``` yaml
# 안 좋은 예
<body>
    <div class="big_strong_text">개발자의 글쓰기</div>
    <div class="blue_text">소프트웨어 엔지니어를 위한 테크니컬 라이팅</div>
    <div class="strong text">개발자라면 이거 모르고 쓰지 마오!</div>
</body>
```
``` yaml
# 안 좋은 예
<body>
    <div class="title">개발자의 글쓰기</div>
    <div class="subtitle">소프트웨어 엔지니어를 위한 테크니컬 라이팅</div>
    <div class="slogan">개발자라면 이거 모르고 쓰지 마오!</div>
</body>
```
``` yaml
# 좋은 예
<body>
    <h1 class="title">개발자의 글쓰기</div>
    <h2 class="title">소프트웨어 엔지니어를 위한 테크니컬 라이팅</div>
    <p class="title">개발자라면 이거 모르고 쓰지 마오!</div>
</body>
```

### Agreeable
- 누가 보더라도 그렇게 짓는 것이 더 낫다고 동의할 수 있는 이름이 좋다.
``` yaml
# 안 좋은 예
for(int i = 0; i < 9; ++i) {
    for(int j = 0; j < 9; ++j) {
        for(int k = 0; k < 9; ++k) {
            for(int l = 0; l < 9; ++l) {
                for(int m = 0; m < 9; ++m) {
```
``` yaml
# 안 좋은 예
for(int indexOfNewEmployeeOfThisMonth = 0; indexOfNewEmployeeOfThisMonth < 9; ++indexOfNewEmployeeOfThisMonth) {
```

### Rememberable
- 같은 단어여도 시청각적으로 기억에 남는 단어가 좋다.
- 개발자만 보는 개발 관련 문서라면 보편적으로 쓰는 이름은 그대로 써도 무방하다.
``` yaml
MPPMAOO         -> POMAMPO
TRQWYE          -> QWERTY
BIE             -> BIOE
Welcome Korea   -> Hello World
```

### Typeable
- 자주 사용되는 이름이라면 입력하기 쉬운지, 오탈자를 낼 가능성이 적은지, 다른 사람에게 말로 전달하기 쉬운지 검토해보자.
``` yaml
# 자판으로 입력할 때 잘 틀리는 단어 예시
- 연속된 철자: successes, classes, committee, parallel
- 묵음: lambda, thumbnail, debt
- ie/ei: chief, receive, retrieve, friends, achieve
- sion/tion: position, commission
- uous/ous/us: continuous, fabulous, genius
```

## 04, 05 주석을 잘 쓰는 법에 관하여 (클린 코드 4장) [참고 링크](https://effortguy.tistory.com/187)

코드로 의도를 표현하라! \
대부분 주석을 보면 코드로 설명이 다 안 되니까 이해시키려고 달아논 코드입니다. \
그러지 말고 코드에 개발자의 의도를 표현하는 방법을 사용하자.

``` yaml
# 직원에게 복지 혜택을 받을 자격이 있는지 검사한다.
if ((employee.flags & HOURLY_FLAG) && (employee.age > 65))
```
if 조건이 아주 길고 어렵기 때문에 위에 주석을 달아논 것을 볼 수 있습니다.

``` yaml
if (employee.isEligibleForFullBenefits())
```
주석을 제거하고 위처럼 의도가 나타나게 코드를 변경하니 주석이 없이도 술술 읽힌다.
<br>

### 좋은 주석
<br>

#### 1. 법적인 주석
``` java
// Copyright (c) 2019, 2020, 2021 by Effort Guy, All rights reserved.
// GNU General Public License 버전 2 이상을 따르는 조건으로 배포한다.
```
코드 배포 license를 명시할 때 사용하는 주석은 소유권 정보로 주석으로 타당하다.
<br>

#### 2. 정보를 제공하는 주석
``` java
// kk:mm:ss EEE, MMM dd, yyyy 형식이다.
Pattern timeMatcher = Pattern.compile("\\d*:\\d*:\\d* \\w*, \\w* \\d*, \\d*");
```
위 주석은 사실 주석이 없어도 이해할 수는 있지만 바로 이해하기 힘들기 때문에 괜찮은 주석이다. \
물론 위처럼 안 하고 메소드로 따로 빼서 의도를 표현한 이름을 사용하면 주석이 필요없을 거 같다.
<br>

#### 3. 의미를 명료하게 밝히는 주석
표준 라이브러리나 변경하지 못하는 코드에 속하는 모호한 인수나 반환값의 의미를 명료하게 밝히는 주석은 괜찮은 주석이다. \
변경할 수 있으면 명확한 이름을 쓰면 된다.
``` java
assertTrue(a.compareTo(a) == 0); // a == a
assertTrue(a.compareTo(b) != 0); // a != b
assertTrue(a.compareTo(b) == -1); // a < b
assertTrue(a.compareTo(b) == 1); // a > b
```
<br>

#### 4. 결과를 경고하는 주석
실행 결과를 미리 경고 하는 주석은 괜찮은 주석이다.
``` java
// 평균 10분 정도 걸리는 작업입니다.
public void calcBalance()...
```
<br>

#### 5. Todo, Fixme 주석
IDE에서 인식할 수 있는 주석을 사용하는 것도 괜찮은 방법이다.
``` java
// Todo : 해야 할 일
// Fixme : 수정 할 작업
```
Todo, Fixme 주석을 달아 놓으면 IDE에서 해당 주석만 몰아서 볼 수 있다.
``` java
// Todo 로그를 추가해야 함
private Order getOrder()...

// Fixme 간헐적으로 디코딩 에러가 발생함
private Student getStudent()...
```
<br>

#### 6. 중요성을 강조하는 주석
자칫 대수롭지 않다고 여겨서 지우거나 수정하면 절대 안 되는 부분에 강조를 위한 주석을 사용한다.
``` java
// 여기서 trim은 반드시 필요하다. 공백으로 시작하는 문자열이 가끔 들어오기 때문이다.
String listItemContent = match.group(3).trim()
```
<br>

#### 7. Javadocs
공개 API나 회사 내에서 공통으로 쓰고 있는 모듈에 달아 놓으면 좋다.
![사진](https://github.com/AlmSmartDoctor/study-2023-10-writing-and-developer/assets/80523328/9d29f665-6b80-4457-9ba8-2b3e709b8d9d) \
위 처럼 javadocs를 달아놓으면 IDE가 아주 깔끔하게 잘 보여준다.
<br>

#### 8. 주석같은 annotation
함수, 변수가 변경되어서 삭제된다는 걸 주석으로도 남길 수 있지만 주석보단 annotation이 더 눈에 띄고 좋다. \
@Deprecated : 어느 시점이후로 사라지게 될 부분이다라는 뜻의 어노테이션 \
아래처럼 Javadocs에 언제부터 없어질지를 적어도 되는데
``` java
@Deprecated(since = "1.3")
```
![사진](https://github.com/AlmSmartDoctor/study-2023-10-writing-and-developer/assets/80523328/2652e9f1-baea-47e3-9e06-c120128171ab) \
이런 식으로 since에 언제부터 사라지는 건지에 대한 시점을 적어줄 수 있다.

이외에도 아래와 같은 것들이 있다.
``` java
@NotThreadSafe : 쓰레드 세이프하지 않다.
@Nullable : Null이 허용된다
@NonNull : Null이 허용되지 않는다.
```
<br>

### 나쁜 주석
작성된 주석 대부분이 나쁜 주석에 포함된다.
<br>

#### 1. 주절거리는 주석
개발자 자신만 알아듣게 주절거리는 식으로 써놓은 주석
``` java
public void loadProperties() {
    try {
        loadedProperties.load(propertiesStream);
    } catch (IOException e) {
        // 속성 파일이 없다면 기본 값을 모두 메모리로 읽어 들였다는 의미다.
    }
}
```
catch에 어떤 작업을 하려고 주석을 달아 놓은 것인가? 아니면 나중에 작업을 하려고 써놓은 주석인가?
확실하지 않기 때문에 로직을 까볼 수 밖에 없다.
이해가 되지 않고 개발자 자신만 아는 말로 써놓는 건 최악이다.
<br>

#### 2. 코드와 동일한 내용을 써놓은 주석
헤더에 달린 주석이 아래 코드 내용과 동일하다. 주석 읽을 시간에 코드 읽는 게 더 빠르다.
``` java
// this.closed가 true일 때 반환되는 유틸
// 타임아웃에 도달하면 예외를 던짐
public synchronized void waitForClose(final long millis) throws Exception {
    if(!closed) {
        wait(millis);
        if(!closed) throw new Exception();
    }
}
```
<br>

##### 3. 애매한 정보가 있는 주석
딱히 예를 들필요가 없다.
주석이 달린 로직을 상세히 적지 않고 오해할만하게 일부만 적은 그런 쓸모없는 주석
<br>

#### 4. 의무적으로 다는 주석
모든 메소드의 인자를 그냥 아무 의미없이 의무적으로 다는 주석은 별로다.
``` java
/**
 * 
 * @param title CD 제목
 * @param author CD 저자             
 */
public void addCD(String title, String author) {
    CD cd = new CD();
    cd.title = title;
    cd.author = author;
    cds.add(cd);
}
```
만약 회사 내부 방침으로 저렇게 다 적어야 한다면 회사 방침을 다시 고려해볼 필요가 있다.
<br>

#### 5. 이력을 기록하는 주석
소스에 주석으로 이력을 관리하는 주석은 별로다.
git이 다 해주기 때문에 불필요하다.
 ``` java
/**
 *
 * 2021년 10월 21일 : 클래스를 정리하고 불필요한 getMember 메소드 삭제
 * 2021년 10월 25일 : getMember 메소드를 다시 추가
 * 2021년 12월 20일 : 클래스 명을 Member -> Customer로 변경
 */
```
<br>

#### 6. 있으나 마나 한 주석
저런 쓸모없는 주석을 다는 사람이 있나?
``` java
// 기본 생성자
protected Member() {}
```
<br>

#### 7. 함수나 변수로 표현할 수 있다면 주석을 달지 마라
``` java
// 직원에게 복지 혜택을 받을 자격이 있는지 검사한다.
if ((employee.flags & HOURLY_FLAG) && (employee.age > 65))
```
  if 조건에 주석을 달지말고 아래처럼 읽자마자 이해가 가게 표현하자.
``` java
if (employee.isEligibleForFullBenefits())
```
<br>

#### 8. 주석으로 처리한 코드
이제는 쓸모없어진? 아니면 잠깐만 주석처리를 해놓은? \
도대체 무슨 의미로 주석처리해놨는지 알 수가 없는 코드는 괜한 오해만 생기게 만든다.
``` java
return getMember();
// updateMember();
// return member;
```
<br>

책엔 더 많은 예제들이 있는데 솔직히 이렇게까지 불필요한 주석을 다는 사람들이 있을까 싶어서 그나마 좀 있을법한 주석 예제들을 넣었습니다. \
사실 이번 장에서 하려는 얘기는 단 하나입니다. \
부정확하고 코드로 나타낼 수 있는 주석은 필요없다. \
정말 필요할 때만 주석을 넣자 정말정말 필요할 때.
