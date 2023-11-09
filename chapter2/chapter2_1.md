# 개발 시간을 줄여주는 이름 짓기와 주석 쓰기

## 01. 네이밍 컨벤션, 이유를 알고 쓰자

### 좋은 이름이란 무엇인가?
- 다른 개발자가 봤을 때 한 번에 무슨 뜻인지, 무슨 기능을 하는지 알아낼 수 있는 이름이다. \

### 이름 짓기는 창조가 아니라 조합이다.
- 기존의 네이밍 컨벤션을 활용하면 고민할 것이 줄어든다. \

### 가독성과 소통이 먼저다.
- 소통의 원활함을 위해 사전에 합의를 해두는 것이 좋다. \

### 각 언어의 네이밍 컨벤션
[Swift 공식 컨벤션](https://www.swift.org/documentation/api-design-guidelines/) \
[TypeScript 구글 컨벤션](https://google.github.io/styleguide/tsguide.html) \

### 네이밍에 간접적으로 도움을 주는 컨벤션들
[Apple 휴먼 인터페이스 가이드](https://developer.apple.com/design/human-interface-guidelines) \
[Apple 개발자 컨퍼런스](https://developer.apple.com/videos/swift) \
[클린 코드](https://www.yes24.com/Product/Goods/11681152) \

---

## 02. 변수 이름을 잘 짓는 법

### i는 변수 이름이지만 d는 아니다.
- i, j, k는 iteration, x, y, z는 coordinate 등으로 흔히 쓰이는 변수명이다. (물론 해당 맥락에서 쓰였을 때)
- 그러나 t, s, d 등의 변수명은 다소 논란의 여지가 있을 수 있다. (생각해보면 모든 변수명은 논란의 여지가 있다.) \

### 약어를 쓰는 것이 좋을까? 안 쓰는 것이 좋을까?
- 용어 정의서에 설명 하나 추가하면 개발 과정이 편해질 수 있다.
- 서비스 이름이나 패키지 이름 등에 쓰는 것은 나쁘지 않다. (AWS, FIR, 등)
- 너무 흔히 쓰이는 약어도 괜찮다. (HTTP, XML, UI, 등) \
 
### 함수 이름 짓는 순서
``` yaml
사용자가 이름을 입력하고 등록 버튼을 클릭하면, 시스템이 사용자 이름을 input 태그에서 가져와 이름 입력 여부와 글자 수를 확인한 후 입력이 안 되었으면 스크립트를 중단하고 input 태그를 활성화해 사용자가 쓸 수 있게 하고, 글자 수가 한글 두 글자 이하면 확인을 요청해 사용자가 확인할 수 있게 해야 한다.
```
``` yaml
1. 사용자가 이름을 input 태그에서 가져온다.
2. 사용자 이름의 글자 수를 확인한다.
3. 입력이 안 되었으면 input 태그를 활성화한다.
4. 글자 수가 한글 두 글자 이하면 확인을 요청한다.
```
``` yaml
1. (함수1) 사용자 이름을 input 태그에서 가져온다.
2. (함수2) 사용자 이름의 글자 수가 2글자 이하면 다음과 같이 처리한다.
  -> 만약 글자 수가0(=null)이면 input 태그를 활성화한다.
  -> 만약 글자 수가 1 또는 2이면 사용자에게 확인을 요청한다.
```
``` yaml
* (함수1) 사용자 이름을 input 태그에서 가져온다.
  -> get user's name from the text input field
* (함수2) 사용자 이름의 글자 수가 2글자 이하면 다음과 같이 처리한다.
  -> do something if user's name contains under 2 characters
```
``` yaml
* (함수1) get user name from input field
* (함수2) check if user name contains under 2 characters
```
``` yaml
* (함수1) getUserNameFromInputField()
* (함수2) checkIfUserNameContainsUnder2Characters()
```
``` yaml
* (함수1) getUserNameFromField()
* (함수2) checkUserNameUnder2Characters()
```
