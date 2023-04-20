# sass for beginner
### sass가 생기게 된 계기
- css 특유의 치명적 단점
  - 규모가 커질수록 코드가 복잡해진다
  - 유지보수가 불편해진다
- 이러한 단점을 보완할 수 있는 것이 sass
- 즉 sass는 코드를 수정하거나, 코드 조각을 재사용하기 편리하다

### sass
- sass(Syntactically Awesome StyleSheets)
- 두 가지 의미
  - css의 단점을 메워 더 빠르고 효율적으로 스타일을 작성할 수 있는 구문
  - css 전처리기(preprocessor)
- 즉 sass는 css 코드를 효율적으로 작성하기 위해 사용하는 프로그래밍 언어이다

### sass 동작 순서
1. sass 구문에 맞게 코드를 작성한다
2. sass 전처리기에 의해 css 코드로 변환된다
3. 변환을 마치고, css 파일이 생성된다

**-> 이러한 과정을 `컴파일`이라고 한다**
  - 이 과정이 필요한 이유?
    - 브라우저는 sass 구문을 이해할 수 없기 때문이다
  - 그럼에도 sass를 쓰는 이유?
    - 간결하고 빠르게 코드를 작성할 수 있기 때문이다

### sass? scss?
- sass 구문과 동일한 기능을 제공함과 동시에 좀 더 css 친화적인 구문이 바로 scss
- scss 구문을 이용해 코드를 작성하면, sass 전처리기는 이 또한 css로 변환
  - 두 코드의 변환 결과는 같음
- 대다수 개발자들은 scss 구문을 선호함
- scss 구문은 sass 언어의 하위 개념

### sass 설치
#### 1. Live sass compiler
- vscode 확장 프로그램 설치
- 해당 scss 파일에서 Watch Sass 클릭하여 실행
- 실행 이후 scss 새로고침하면 자동으로 css에 적용 (주의! 생성된 css 파일은 웬만하면 직접 건드리지 말것)

#### 2. 명령행 인터페이스 방식
- node.js 설치
- 터미널에서 `npm install -g sass` 명령어 실행
- 해당 scss 빌드 할 폴더 경로에서 터미널에 다음과 같이 입력
- `sass 빌드할scss경로:빌드후생성될css경로`
    - ex) `sass style/main.scss:style/main.css`
- 라이브로 계속 변화를 감지해서 적용하고 싶다면 다음과 같이 `--watch`추가
    - ex) `sass --watch style/main.scss:style/main.css`
    - 라이브 종료는 `ctrl + c`
- 공백 없이 convention에 맞추어 작업하고 싶은 경우는 다음과 같이 `--style compressed` 추가
    - ex) `sass --style compressed style/main.scss:style/main.css`
    - `--watch` 와 같이 사용하고 싶은 경우엔 `--watch` 뒤에 와야함