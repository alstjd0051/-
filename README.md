1년간 프론트엔드를 공부하며 참고했던 문서를 정리했습니다.

'필수'로 표시된 문서엔 이 프로젝트를 개발하는데 필요한 지식이 담겨있기 때문에 꼭 읽어 보고, 그 외 문서는 시간날 때 들어가서 읽는 것을 권장합니다. 문서를 읽을 땐 아는 내용은 건너뛰고 모르는 부분 위주로 읽고, 특히 어려운 내용 관련해선 심도 있게 읽어 보는 것을 권장합니다.

# Git

- https://backlog.com/git-tutorial/kr/intro/intro1_1.html (필수)

# JavaScript

- [JavaScript Info (파트 1) **(필수)**](https://ko.javascript.info/)
- 안희종의 [타입스크립트 기초](https://ahnheejong.gitbook.io/ts-for-jsdev/) (2단원 전체)
- [MDN JavaScript](https://developer.mozilla.org/ko/docs/Web/JavaScript) (레퍼런스)
- ECMAScript [표준 논의 과정](https://ahnheejong.name/articles/ecmascript-tc39/) - Stage 0 : 아이디어 제안 - Stage 1 : 기획 중 - Stage 2 : 개발 중 - Stage 3 : 테스트 중 - Stage 4 : 완성 (다음 버전에 출시)
  3단계부터 출시 확정이라고 볼 수 있다.

# TypeScript

만약에 타입스크립트를 한번도 써보지 않았거나 조금만 써봤다면 밑의 모든 글을 읽고 따라해보는 것을 권장합니다. 또한 타입스크립트 공식 문서가 워낙 잘 정리되어 있으니 공식 문서도 한 번 보는걸 권장합니다.

## TypeScript 기초

- 안희종의 [타입스크립트 기초](https://ahnheejong.gitbook.io/ts-for-jsdev/) (3단원 전체) (필수)
- [타입스크립트 공식 문서](https://www.typescriptlang.org/)
- [Velopert의 타입스크립트 기초](https://velog.io/@velopert/using-react-with-typescript)

  ### TypeScript 개발 환경 설정

  - tsc(TypeScript Compiler), Webpack, ESLint, Prettier 연동

  ### TypeScript 심화

- TypeScript의 [장단점](https://www.rinae.dev/posts/fear-trust-and-javascript-kr)
- TypeScript로 [Todo 리스트 만들기](https://ts.chibicode.com/todo/)
- https://basarat.gitbook.io/typescript/

- https://www.typescriptlang.org/docs/handbook/declaration-files/deep-dive.html

- [유니온 타입을 통한 안전한 데이터 모델링 (안희종)](https://ahnheejong.name/articles/safe-data-modeling-using-disjoint-union-type/)
- [실용적인 고급 TypeScript (rinae.dev)](https://www.rinae.dev/posts/practical-advanced-typescript-summary)

- Omit, Pick, Partial Type 활용하기

  - https://www.typescriptlang.org/docs/handbook/utility-types.html
  - https://rinae.dev/posts/helper-types-in-typescript

- [TypeScript 공식 업데이트 블로그(Microsoft)](https://devblogs.microsoft.com/typescript/)
  [- TypeScript Tuple 고급](https://blog.cometkim.kr/posts/typescript-tuples/)
- [TypeScript에게 내 의도를 이해시키는 방법 (YouTube)](https://www.youtube.com/watch?v=bfSKqscC8kc&feature=youtu.be&fbclid=IwAR1SX5jELndrr1_0C26I3jmS_5L1sEW8_PRqiF-xPfBVyXmJE_DIwz1CVWk)

- JavaScript, TypeScript 순환 [참조 해결하기(rinae.dev)](https://www.rinae.dev/posts/fix-circular-dependency-kr)

## 함수형 프로그래밍

- https://dev.to/fannyvieira/the-beauty-of-functional-programming-32ck
- https://dev.to/mr_bertoli/an-adequate-introduction-to-functional-programming-1gcl
- https://dev.to/benlesh/a-simple-explanation-of-functional-pipe-in-javascript-2hbj
  Immutable data structures for functional JS (YouTube)
  Functional Programming in JS: What? Why? How? (YouTube)

## 함수형 프로그래밍 기초

- 유인동의 인프런 함수형 강의 (좋은 강이의지만 너무 맹신하진 말 것)
- 함수형 프로그래밍을 사용하는 이유 (장단점)
- 함수형 프로그래밍 활용 예시 (rinae.dev)

## 함수형 프로그래밍의 중요한 개념

- Immutability, Pure funciton, Side effect (필수)
- Memoization (필수)
- Declarative vs imperative programming
- First class citizen
- Higher Order functions, Lambda function, Closure
- Function composition
- Currying, Pipelining
- e.g. `map, filter, reduce` (필수)

## 함수형 프로그래밍 라이브러리

- lodash
- Ramda

## React, TypeScript와 함께 쓰는 함수형 프로그래밍

### Stale States 개념과 주의사항

# React

## React 기초

- React 공식 문서 (설치, 주요 개념 전부) (필수)

## React 심화

- React 내부 작동 원리
- 함수형 컴포넌트와 Class 컴포넌트의 차이
- React 관련 블로그(영어)

## React Hooks

- React Hooks 공식 문서 (Hook 전부) (필수)
- Hooks 호출 순서가 중요한 이유
- Side Effect: useEffect 작동 원리

  - https://rinae.dev/posts/a-complete-guide-to-useeffect-ko
  - https://rinae.dev/posts/getting-closure-on-react-hooks-summary

- Memoization: useMemo, useCallback 작동 원리

  - https://kentcdodds.com/blog/usememo-and-usecallback
  - When to use useMemo and useCallback (rinae.dev)
  - Closure?: useState, useReducer 작동 원리

## React ref 이해

## 확장 프로그램

- React 개발자 도구 [(크롬)](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)

# Next

## 페이지 라우팅 (필수)

#### React의 `react-router-dom`과 역할이 비슷

- https://nextjs.org/docs/basic-features/pages (Pre-rendering 전까지, 3~5분)
- https://nextjs.org/docs/routing/introduction (전체, 10~20분)
- https://nextjs.org/docs/routing/dynamic-routes (전체, 10~20분)

## Next 심화

- Next로 앱을 만들면서 배운 점
- Next Tutorial 따라하기
- Create React App과 Create Next App의 차이점 (SSR, CSR)

## 브라우저 및 웹

- [서버, 클라이언트 계층 구조](https://www.stevenjlee.net/2020/05/08/%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-3%EA%B3%84%EC%B8%B5-%EA%B5%AC%EC%A1%B0-3-tier-architecture/)
- [브라우저 내부 작동 원리 (D2)](https://d2.naver.com/helloworld/59361)
- HTTP Caching [MDN](https://developer.mozilla.org/ko/docs/Web/HTTP/Caching)
- HTTP Caching [Google](https://web.dev/http-cache/)
- HTTP [요청-응답](https://blog.outsider.ne.kr/888) 구조 이해
- HTTP Header [MDN](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers) → 실제 사이트에서 크롬 개발자 도구의 Network 탭에서 Request를 확인
- [Node.js 이벤트 루프 내부 원리 (블로그)](https://evan-moon.github.io/2019/08/01/nodejs-event-loop-workflow/)

### Testing

#### Unit Test

- Unit Test란?
- Jest

#### Snapshop Test

- Snapshop Test란?

#### E2E Test

- E2E Test란?

### GraphQL

#### GraphQL 입문

- https://tech.kakao.com/2019/08/01/graphql-basic/

이 블로그 글을 읽고 GraphQL이 무엇이고 왜 사용하는지 감을 잡습니다. (약 30분 소요)

### GraphQL 기본 개념

- https://graphql.org/learn/
  공식 GraphQL 문서의 Introduction을 읽고 정확한 정의를 이해합니다. Introduction만 읽고, 나머지는 필요할 때 읽습니다. (약 30분 소요)

GraphQL Fundamentals Tutorial

- https://www.howtographql.com/basics/0-introduction/
  GraphQL 의 코어를 동영상 강의로 익혀봅니다. (약 2시간 소요)

## GraphQL 심화

- [REST vs GraphQL (Apollo Blog)](https://www.apollographql.com/blog/graphql/basics/graphql-vs-rest/)
- [GraphQL Schema로부터 TypeScript의 type 자동 생성하기 (React-Apollo Hooks)](https://www.graphql-code-generator.com/)
- GraphQL 을 사용하기 위해 Apollo 외에 사용할 수 있는 것들은 무엇이 있는지? 각 도구의 특징 비교. (Relay 등)

# Apollo

Apollo 공식 문서
Apollo가 무슨 기능을 제공하고, Apollo Client와 Apollo Server는 무엇이 다른지 생각해보기 (약 5시간 소요)

- [튜토리얼](https://www.apollographql.com/docs/tutorial/introduction/)
- **(필수)**[Fetching, Caching](https://www.apollographql.com/docs/react/)
- [Integration, Migration 제외) (심화)](https://www.apollographql.com/docs/react/)

## Apollo Client (React) Tutorial

https://www.howtographql.com/react-apollo/0-introduction/

- Hackernews 를 만들어보면서 위에서 익힌 GraphQL의 개념을 적용해보고, Apollo Client (React)의 기본적인 사용법을 익혀봅니다. (약 5시간 소요)

## Storybook

컴포넌트 API 문서와 컴포넌트 props 테스트 페이지를 자동으로 생성해주는 개발 도구

## React Hook Form

input element의 상태를 관리해주는 패키지
