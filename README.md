# java-racingcar-precourse

![JDK Version](https://img.shields.io/badge/JDK-21-blue.svg)

<img src="https://i.ibb.co/ScdBqFT/logo-light.png" alt="프로젝트 이미지"/>

```
우아한테크코스 7기 프리코스 2주차 - 자동차 경주 구현 내용을 담고 있습니다.
```

---

- [과제 요구사항](#과제-요구사항)
- [기능 목록](#기능-목록)
- [프로그래밍 요구사항](#프로그래밍-요구사항)
- [실행 결과 예시](#실행-결과-예시)

### 과제 요구사항

1. 기능 목록을 README.md에 구현한 후 구현을 시작한다.
2. commit 단위는 위 기능 목록을 기준으로 추가한다.
3. commit은 [AngularJS Git Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153) 참고하여
   작성한다.

### 기능 목록

- 사용자 입력
    - 사용자가 입력하는 값은`camp.nextstep.edu.missionutils.Console`의`readLine()`을 활용한다.
    - 사용자는 경주할 자동차 이름을 쉼표(,) 기준으로 구분하여 입력한다.

        ```java
        pobi,woni,jun
        ```

    - 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.

        ```java
        5
        ```

    - 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 어플리케이션은 종료 되어야 한다.
- 자동차 입력
    - 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
    - 자동차 이름은 쉼표(,)를 기준으로 구분한다.
    - 이름은 5자 이하만 가능하다.
- 자동차 이동
    - 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
    - 전진하는 조건은 0부터 9사이 무작위 값을 구한 후 무작위 값이 4 이상일 경우다.
    - Random 값 추출은`camp.nextstep.edu.missionutils.Randoms`의`pickNumberInRange()`를 활용한다.
    - 자동차 이동 차수별 실행결과를 출력한다.

        ```java
        pobi : --
        woni : ----
        jun : ---
        ```

- 우승자 출력
    - 자동차 경주 게임을 완료한 후 누가 우승했는지 알려준다.
    - 우승자는 한 명 이상일 수 있다.
    - 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
    - 단독 우승자 안내 문구

        ```
        최종 우승자 : pobi
        ```

    - 공동 우승자 안내 문구

        ```
        최종 우승자 : pobi, jun
        ```

### 프로그래밍 요구사항

- `build.gradle`파일은 변경할 수 없으며,**제공된 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.**
- 프로그램 종료 시`System.exit()`를 호출하지 않는다.
- 함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게 만들어라.
- 3항 연산자를 쓰지 않는다.
- indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
- JUnit 5와 AssertJ를 이용하여 정리한 기능 목록이 정상적으로 작동하는지 테스트 코드로 확인한다

### 실행 결과 예시

```bash
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
gray,son,bang
시도할 횟수는 몇 회인가요?
3
실행 결과
gray : -
son : -
bang : -

gray : -
son : -
bang : --

gray : -
son : -
bang : ---

최종 우승자 : bang
```
