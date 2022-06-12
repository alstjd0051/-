# TypeScript

만약에 타입스크립트를 한번도 써보지 않았거나 조금만 써봤다면 밑의 모든 글을 읽고 따라해보는 것을 권장합니다. 또한 타입스크립트 공식 문서가 워낙 잘 정리되어 있으니 공식 문서도 한 번 보는걸 권장합니다.

## TypeScript 기초

- 안희종의 [타입스크립트 기초](https://ahnheejong.gitbook.io/ts-for-jsdev/) (3단원 전체) (필수)
- [타입스크립트 공식 문서](https://www.typescriptlang.org/)
- [Velopert의 타입스크립트 기초](https://velog.io/@velopert/using-react-with-typescript)

## TypeScript 개발 환경 설정

- tsc(TypeScript Compiler), Webpack, ESLint, Prettier 연동

## TypeScript 심화

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

- 유인동의 인프런 함수형 강의
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

# JSX.Element vs ReactNode vs ReactElement의 차이

- 클래스형 컴포넌트는 render메소드에서 ReactNode를 리턴한다.
- 함수형 컴포넌트는 ReactElement를 리턴한다.
- JSX는 바벨에 의해서 React.createElement(component, props, ...children) 함수로 트랜스파일된다.

## ReactElement

```typescript
interface ReactElement<
  P = any,
  T extends string | JSXElementConstructor<any> =
    | string
    | JSXElementConstructor<any>
> {
  type: T;
  props: P;
  key: Key | null;
}
```

`React.createElement를 호출하면 이런 타입의 객체가 리턴한다.`

## ReactNode

```typescript
type ReactText = string | number;
type ReactChild = ReactElement | ReactText;

interface ReactNodeArray extends Array<ReactNode> {}
type ReactFragment = {} | ReactNodeArray;

type ReactNode =
  | ReactChild
  | ReactFragment
  | ReactPortal
  | boolean
  | null
  | undefined;
```

`ReactNode는 ReactElement의 superset이다. ReactNode는 ReactElement일 수 있고 null, undefined, boolean 등등.. 좀 더 유연한 타입 정의라고 할 수 있다.`

## JSX.Element

```typescript
declare global {
  namespace JSX {
    interface Element extends React.ReactElement<any, any> {}
  }
}
```

`JSX.Element는 ReactElement의 특정 타입이라고 생각하자. 또한 글로벌 네임스페이스에 정의되어 있어 외부 라이브러리에서 이 JSX.Element를 재정의할 수 있다.`
