### 설치
```js
$ pnpm vite create // react typescript swc, 경로 ./
$ pnpm i
$ pnpx storybook@latest init
```

### 실행
```js
$ pnpm run dev /* 서버 */
$ pnpm run storybook /* 스토리북 */
$ pnpm run deploy /* 배포 (호스팅) */
$ pnpm run chromatic /* 배포 (스토리북) */
```

### 경로
호스팅(https://rightbrainlib.github.io/template/)<br />
스토리북(https://www.chromatic.com/builds?appId=658a6bfc7dd28e3bfc8cf29a)

...

# comments rule

| 요약> vsc_snippets 폴더의 json 파일을 아래에 명시한 설치 경로에 붙여놓고<br /> VSC에서 `cmt` 입력 후 ctrl + space로 원하는 주석 활용<br /><br />
*block comment*<br />
코드 작성시 wrapper 와 같이 감싸는 부분의 블럭을 쉽게 구분하기 위해 사용

*explain comment*<br />
코드 작성시 해당 부분의 용도나, parameter, return값 등 디버깅에 참고할 만한 내용들

*기타 comment*<br />
반복 사용되는 내용을 룰로 정함

룰로 정하지 않은 내용은 자유롭게 활용
<br />
## vsc_snippets json 파일 설치 경로
`C:\Users\RB-N-168\AppData\Roaming\Code\User\snippets`
<br />
<br />
## CSS, SCSS 주석
#### block 주석
*prefix: cmt-block*
```
/* S: gnb */
.gnb
/* E: gnb */
```
#### 설명 주석
*prefix: cmt-explain*
```
/* [C: 설명 시작 */
css 코드 작성...
/* C]: 설명 끝 */
```
#### scss 변수 주석
*prefix: cmt-variable*
```
/* <VAR: 색상 모음 */
$main-color: #345678;
/* VAR>: 색상 모음 */
```

#### scss mixin 주석
*prefix: cmt-mixin*
```
/* <MIX: util 모음 */
@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, .25);
  color: #fff;
 }
/* MIX>: util 모음 */
```

#### scss extend 주석
*prefix: cmt-extend*
```
/* <EXT: extend 모음 */
%extend {

}
/* EXT>: $1 */
```

#### scss keyframes 주석
prefix: cmt-keyframes
```
/* <kf: bounce 애니메이션 */
@keyframes bounce {
	// ...생략
}
/* kf>: bounce 애니메이션 */
```

#### scss media-query 주석
*prefix: cmt-media*
```
/* <media: 360이하 */
@media screen and (max-width: 360px) {
  // ...생략
}
/* media>: 360이하 */
```

## JS, react 주석
#### block 주석
*cmt-block*
```
{/* S: card-box */}
// ... 생략
{/* E: card-box */}
```

#### 설명 주석
*prefix: cmt-explain*
```
{/* 설명글 */}
// ... 생략
{/* // 설명글 */}
```

#### modal 주석
*prefix: cmt-modal*
```
{/* S: $1-modal */}
// ... 모달 작성 ...
{/* E: $1-modal */}
```

#### 함수 주석
*prefix: cmt-function*
```
/**
 * [setCalendarDate
 * 기능: 선택한 날짜로 달력 활성화하기",
 * @parameter year: number, date: number, day: number",
 * @return dateStr: number",
 */
const setCalendarDate = (year, date, day) => {",
  // ... 구현
  return dateStr;
};
/* setCalendarDate] */
```

## html 주석
#### block 주석
*prefix: cmt-block*
```
<!-- S: gnb -->
<div class="gnb">
// ...생략...
</div>
<!-- E: gnb -->
```
#### 설명 주석
prefix: cmt-exp
```
<!-- [설명 제목] -->
[설명 내용 작성]
```
#### modal 주석
prefix: cmt-modal
```
<!-- S: login-modal -->
<div class="login-modal>
// ...생략...
</div>
<!-- E: login-modal -->
```
