# CH03 - Javascript Starter Kit_Hacker News Client

- 해당 챕터에서는 강의내용에 집중 (코드 관련은 예제 코드 적용)

1. HackerNews클라이언트앱
2. 12줄의코드로시작하기
3. 두개의화면을가진웹앱
4. 문자열을활용한HTML다루기
5. 라우터？화면처리기만들기
6. 페이징구현하기
7. 복잡한UI구현을위한준비작업-템플릿
8. 댓글목록이표시되는아름다운UI만들기, 상태를가져보자,읽은글표시하기

- 자바스크립트 클라이언트 앱을 간단하게 구축하는 방법과 간략하게 라우터 및 상태를 다뤄보는 강의였다. 복잡도에 대해서 조금더 생각하게되는 강의였다. 내가 실무에서 과연 복잡도에 대한 고민을 얼마만큼하고 개발을 하고있는지 자신을 되돌아보는 계기가 되었다. 규모가 커지면 당연히 코드에 대한 크기도 커지기도 하는데 반복되는 코드들에 대한 생각을 내가 얼마만큼 했는지 되돌아보았고
  어느순간 기능에만 집중하여 복잡도에 대한 고민을 덜 했던 나 자신을 되돌아보는 계기가 되었다.

# CH04 - Typescript Start Kit_Hacker News 마이그레이션

1. 타입스크립트를 위한 환경 설정

- 타입스크립트로 마이그레이션 진행하기전 환경 설정을 진행
- tsconfig.json 파일을 생성

2. 변수에 타입 작성하기

- 타입 알리아스

```typescript
type Store = {
  currentPage: number;
};
```

- 인터페이스 -> interface

```typescript
  interface Store : {
    currentPage: number
  }
```

- 타입가드 코드 작성하는 습관가지기

3. 함수의 규격 작성하기

- Extension -> Rest Client 설치
  - .http파일 작성 send.request 실행시 값을 vsCode에서 확인 가능

4. 타입과 인터페이스

- 인터페이스 방법으로 타이핑
- 다른 값으로 대체 불가능하게 하려면 readonly 지시어 활용가능

```typescript
  interface Store : {
    currentPage: number
  }

  interface News {
    readonly id: number;
    readonly time_ago: string;
    readonly title: string;
    readonly url: string;
    readonly user: string;
    readonly content: string;
  }
```

5. 상속과 믹스인

- 상황에 따라서 개발자 성향에 따라서 사용하는 방법이 달라진다고함
- 믹스인 문법은 처음 접해봐서 좀 신선했음 -> 아직 모르는 부분이 많구나라는 생각을 함

6. 뷰 클래스로 코드 구조 개선

- 함수로 되어있는 코드를 class로 변환 작업 진행
- 클래스는 이름을 대문자로 시작하는 컨벤션 규칙을 지키자
  - 일반 함수 호출과는 구분되어야 되기때문에 첫글자 대문자 컨벤션을 지키는게 맞다고 생각한다.
- 외부에서 접근할 필요가 없는 메소들이나 속성들을 굳이 public으로 할 필요가 없다.

7. 파일의 분리, 더욱 성장할 앱을 위한 준비

8. 안전한 전역 상태 관리

9. XHR to Fetch & Promise

- 비동기 코드로 교체
- addEventListener 받은 데이터를 콜백함수로 데이터를 넘겨줘야함

10. 콜백 함수 없는 비동기 코드 작성법

- async await 사용
- tsconfig - lib : ["es6","dom"] 추가

- 초반에는 어느정도 아는 부분이여서 코드 작성보다 설명위주로 강의를 보았는데 후반 부로 갈수록 클래스로 교체작업 진행할때 함수 컴포넌트가 아닌 클래스 컴포넌트로 작성해서 재밌게 강의를 들을 수 있었다.
  강의에서 간략하게 설명해주었는데 핵심만 뽑아서 설명해주어 각인이 잘되었다. 처음엔 편하게 들어야지 생각을 가졌다가 중후반 부로 갈수록 편하게 들을수가 없어서 집중을 할 수 밖에 없는 나의 모습을보고 강의가 알짜배기구나 라는 생각을 가지게되었다.
