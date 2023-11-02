# 개발자는 글을 못 쓴다?

- 보통 기획자나 관리자는 개발자가 글을 못 쓴다고 생각한다.\
-> 기획서나 전략보고서 같은 글을 개발자에게 요구하면 당연히 잘 못 쓸 수 밖에 없다
- 개발자는 프로그램 안에서 글을 쓰거나 개발 완료 후 결과서나 산출물을 주로 쓴다

<br/>

>기획자나 관리자의 글쓰기는 논리력, 설득력, 실행력이 중요하다면,\
**개발자의 글쓰기에는 정확성, 간결성, 가독성이 중요하다**

<br/>

# 개발자 글쓰기의 특징: 정확성, 간셜성, 가독성

- 정확성: 틀림이 없이 확실한 것; 글로 쓰인 대로만 개발하면 버그 X
- 간결성: 글에 군더더기가 없고 간단하고 깔끔한 것; 구구절절 설명 X, 핵심만
- 가독성: 쉽게 읽히는 것; 쉬운 용어, 표, 그림, 문단과 문서 전체에 체계와 위계

<br/>

- # 문제점 - 세 가지 원칙이 서로 대치
    - 정확성을 높이면 간결성, 가독성 낮아진다.
    - 간결성을 높이면 정확성, 가독성 낮아진다.
    - 가독성을 높이면 정확성, 간결성 낮아진다.


    <details>
    <summary>예시: 신청자의 나이로 성인인지 아닌지 분류하는 코드</summary>

    ``` javascript
    function get(m) {
        var result;
        if (m.year < 20) {
            result = 0;
        } else {
            result = 1;
        }
    }
    ```

    하지만 우리나라 민법의 성년 기준은 20세가 아닌 만 19세

    - 간결성 &uarr;
        ``` javascript
        function get(m) {
            var result;
            var todayMonthAndDay = ... 
            if (m.year > 19) {
                result = 1;
            } else if (m.year === 19) {
                if (m.monthAndDay >= todayMonthAndDay) {
                    result = 1;
                } else {
                    result = 0;
                }
            } else {
                result = 0;
            }
        }
        ```

        if 문으로 간결해졌지만, 지나친 `result =` 으로 정확성  &darr;, 가독성도  &darr;

    - 정확성 &uarr; & 가독성 &uarr; 
        ``` javascript
        const LEGAL_ADULT = 1;
        const LEGAL_NOT_ADULT = 0;

        function get(m) {
            var legalAdult;
            if (m.ageOfMajority > 19) {
                result = LEGAL_ADULT;
            } else if (m.ageOfMajority === 19) {
                if (m.monthAndDay >= todayMonthAndDay) {
                    result = LEGAL_ADULT;
                } else {
                    result = LEGAL_NOT_ADULT;
                }
            } else {
                result = LEGAL_NOT_ADULT;
            }
        }
        ```

        정확성, 가독성은 높아졌지만, 간결성 &darr;
    </details>

<br/>

# 개발자의 글쓰기

- 아무도 개발자의 글쓰기에 대해 신경 쓰지 않고, 배우기 쉽지 않다
- 요즘은 깃허브 등을 통해 개발자가 만든 코드를 공개하고, 개발자 사이트를 통해 외부 개발자와 협력하는 일이 늘었다
- 이 책을 통해 함수/변수 이름 짓기, 주석, 에러 메시지 쓰는 법, 릴리스 노트, 장애 보고서, 개발 가이드, SI 제안서, 개발 블로그 운영 팁 등을 배워라
- 코딩과 마찬가지로 글쓰기도 과학이고 기술이므로, 누구나 체계적으로 배우기만 하면 글을 잘 쓸 수 있다.


