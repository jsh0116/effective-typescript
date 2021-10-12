## Item 3 : 코드 생성과 타입이 관계없음을 이해하기

**Typescript Compiler의 역할** 

- 최신 TS/JS를 Browser에서 동작할 수 있도록 구버전 JS로 transpile(translate + compile)
- Code의 Type Error check

**Typescript가 할 수 있는 일과 할 수 없는 일**

* Type Error가 있는 Code도 Compile이 가능하다

  * Typescript에서 Compile은 Type check와 독립적으로 동작하기 때문에 Type error인 code도 compile 가능
  * example
    
    * 테스트 코드 확인
    ```bash
      $ cat test.ts
    ```
    * Typescript Complie
    ```bash
      $ tsc test.ts
    ```
    * 위 작성한 명령어를 통해 type check에 문제가 있다는 것을 확인할 수 있다
  
  * Compile과 Type check
    * Typescript에서 code error가 있을 때 `Compile에 문제가 있다` 라는 말은 기술적으로 잘못된 표현
    * 엄밀히 말하면 code 생성만이 'compile'이라고 말할 수 있기 때문이다
    * 따라서 `type check에 문제가 있다`라는 표현이 정확한 표현

* Runtime에는 Type Check가 불가능하다


* Type 연산은 Runtime에 영향을 주지 않는다


* Runtime Type은 선언된 Type과 다를 수 있다


* Typescript Type으로는 함수를 override할 수 없다.


* Typescript Type은 Runtime 성능에 영향을 주지 않는다.