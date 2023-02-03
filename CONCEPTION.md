### 식별자

> 식별자는 데이터가 될 수 없지만 데이터를 코드화 할 수 있다.
> 이때는 식별자 명명 규칙을 따르지 않아도 된다. (공백이나 문자열 포함 가능)

```
const o={
  age:10,
  ['myName']='윤',
}

o.myName 으로 접근할 수 있다.

단, 공백을 포함했을 때는 o.['my Name'] 식으로 접근 할 수 있다.
```

<br/>

### 타입

> 자바스크립트 변수 타입은 값을 넣는 순간 결정이 된다. 편리하지만 예외처리를 해야하는 등 버그를 만들기 쉬운 언어가 될 수 있다.

> 타입스크립트는 지정한 타입만 변수에 할당할 수 있는데 런타임이 아닌 '컴파일 타임'에 오류를 잡아내 준다고 하는 것이 큰 가치라고 할 수 있다.

<br/>

### 변수와 상수

```
변수: 한번 만들어 놓은 후에 그 변수가 가지고 있는 값을 다른 값으로 변경할 수 있다.

상수: 최초에 만들어질 때 단 한 번만 값을 넣을 수 있고 그 이후에는 값을 바꾸지 못한다.
```

### 배열 연산

**map**
<br/>
map을 실행 할 때 코드를 따로 밖으로 빼놓으면 표현력도 좋아지고 재사용성도 좋아진다.
(일급함수 활용)

```
<예시>

const bookTitleBookObject = (book) => ({ title: book });
const makeAuthor = (name) => (book) => ({
  ...book,
  author: name
});

const shakespeareTwoBooks = books
  .map(bookTitleBookObject)
  .map(makeAuthor("William Shakespeare"));

```

**reduce**

```
const someNumbers: number[] = [ 10, 5, 8, 3, 2 ];

const sumNumber = someNumbers.reduce((a: number, b: number) => a + b, 0);
```

### 튜플

> 배열인데 원소의 개수를 제한하고 그 각각의 원소의 타입을 규정한 데이터 타입,
> 크기가 고정된 배열을 쓸 때, 튜플로 만들어 주면 타이핑의 영역을 훨씬 더 확장할 수 있다.

```
const address : [number, string, string] = [940315, '서울시', '송파구']
```
