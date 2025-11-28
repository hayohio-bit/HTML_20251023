## 주요 태그


**텍스트/제목 태그**

| 태그 | 용도 | 대표 속성 |
| --- | --- | --- |
| `<h1>`~`<h6>` | 제목 (1단계~6단계) | id, class |
| `<p>` | 단락 | id, class |
| `<span>` | 인라인 텍스트 그룹 | id, class, style |
| `<br>` | 줄바꾼 (닫는 태그 없음) | - |
| `<strong>` | 굵게 (중요도 강조) | - |
| `<em>` | 기울임 (강조) | - |


**링크/이미지 태그**

| 태그 | 용도 | 대표 속성 |
| --- | --- | --- |
| `<a>` | 하이퍼링크 | href, target, title |
| `<img>` | 이미지 삽입 | src, alt, width, height |


**리스트 태그**

| 태그 | 용도 | 대표 속성 |
| --- | --- | --- |
| `<ul>` | 순서 없는 목록 | type |
| `<ol>` | 순서 있는 목록 | type, start |
| `<li>` | 목록 항목 | value |

**폼 태그**

| 태그 | 용도 | 대표 속성 |
| --- | --- | --- |
| `<form>` | 폼 컨테이너 | action, method |
| `<input>` | 입력 필드 | type, name, value, placeholder |
| `<textarea>` | 다줄 텍스트 | rows, cols, name |
| `<button>` | 버튼 | type, name, disabled |
| `<select>` | 드롭다운 | name, multiple |
| `<option>` | 선택 항목 | value, selected |
| `<label>` | 레이블 | for |


**테이블 태그**

| 태그 | 용도 | 대표 속성 |
| --- | --- | --- |
| `<table>` | 테이블 컨테이너 | border |
| `<tr>` | 테이블 행 | - |
| `<td>` | 테이블 셀 | colspan, rowspan |
| `<th>` | 테이블 헤더 셀 | colspan, rowspan, scope |
| `<thead>` | 헤더 영역 | - |
| `<tbody>` | 본문 영역 | - |
| `<tfoot>` | 푸터 영역 | - |


**구조/시맨틱 태그**
```
+------------------------------------------+
|  <header>  사이트 상단 (로고, 네비)       |
+------------------------------------------+
|  <nav>  메인 네비게이션                  |
+------------------------------------------+
|  <main>                                  |
|    +------------------+  +-----------+   |
|    | <section>        |  | <aside>   |   |
|    | 메인 콘텐츠       |  | 사이드바  |   |
|    +------------------+  +-----------+   |
+------------------------------------------+
|  <footer>  사이트 하단 (저작권, 링크)     |
+------------------------------------------+


```
| 태그 | 용도 | 설명 |
| --- | --- | --- |
| `<div>` | 블록 구역 | 레이아웃 및 그룹화 |
| `<header>` | 헤더 영역 | 페이지/섹션 상단 |
| `<nav>` | 네비게이션 | 메뉴 영역 |
| `<main>` | 메인 콘텐츠 | 페이지 핵심 콘텐츠 |
| `<section>` | 섹션 | 주제별 콘텐츠 구분 |
| `<article>` | 독립 콘텐츠 | 블로그 글, 뉴스 기사 |
| `<aside>` | 사이드바 | 보조 콘텐츠 |
| `<footer>` | 푸터 영역 | 페이지/섹션 하단 |


**주요 input type 정리**

| type | 용도 | 예시 |
| --- | --- | --- |
| text | 한 줄 텍스트 | 아이디, 이름 |
| password | 비밀번호 (마스킹 처리) | 로그인 |
| email | 이메일 형식 검증 | 이메일 주소 |
| number | 숫자 입력 | 나이, 수량 |
| date | 날짜 선택 | 생년월일 |
| checkbox | 체크박스 | 동의 여부 |
| radio | 라디오 버튼 | 단일 선택 |
| file | 파일 업로드 | 이미지 업로드 |
| submit | 제출 버튼 | 폼 제출 |

---
- **선택자(Selector)**
    - 
    - *선택자(Selector)**는 스타일을 적용할 HTML 요소를 선택하는 패턴입니다.
    
    **CSS 기본 문법**
    
    ```css
    선택자 {
      속성: 값;
      속성: 값;
    }
    
    ```
    
    **주요 선택자 종류**
    
    | 선택자 | 문법 | 설명 | 예시 |
    | --- | --- | --- | --- |
    | 전체 | `*` | 모든 요소 | `* { margin: 0; }` |
    | 태그 | `태그명` | 해당 태그 모두 | `p { color: red; }` |
    | 클래스 | `.클래스명` | class 속성 값 | `.title { font-size: 20px; }` |
    | 아이디 | `#아이디` | id 속성 값 | `#header { height: 100px; }` |
    | 자손 | `부모 > 자식` | 직계 자식만 | `ul > li { list-style: none; }` |
    | 후손 | `조상 후손` | 모든 후손 | `div p { color: blue; }` |
    | 인접 형제 | `A + B` | 바로 다음 형제 | `h1 + p { margin-top: 0; }` |
    | 가상 클래스 | `:hover` | 마우스 올림 시 | `a:hover { color: red; }` |
    | 가상 요소 | `::before` | 콘텐츠 삽입 | `p::before { content: "●"; }` |
    | 속성 | `[attr]` | 속성 유무 | `input[type="text"] { }` |
- **박스 모델(Box Model)**
    - 
    
    **박스 모델**은 모든 HTML 요소를 감싸는 상자 구조입니다.
    
    **박스 모델 구성 요소**
    
    ```
    +------------------------------------------+
    |              margin (외부 여백)            |
    |  +--------------------------------------+  |
    |  |           border (테두리)            |  |
    |  |  +--------------------------------+  |  |
    |  |  |        padding (내부 여백)       |  |  |
    |  |  |  +------------------------+  |  |  |
    |  |  |  |      content (내용)     |  |  |  |
    |  |  |  +------------------------+  |  |  |
    |  |  +--------------------------------+  |  |
    |  +--------------------------------------+  |
    +------------------------------------------+
    
    ```
    
    **주요 속성**
    
    | 속성 | 설명 | 예시 |
    | --- | --- | --- |
    | `width/height` | 콘텐츠 너비/높이 | `width: 300px;` |
    | `padding` | 내부 여백 | `padding: 10px 20px;` |
    | `border` | 테두리 | `border: 1px solid #000;` |
    | `margin` | 외부 여백 | `margin: 0 auto;` |
    | `box-sizing` | 크기 계산 방식 | `box-sizing: border-box;` |
    
    **box-sizing 속성**
    
    - `content-box` (기본): width/height = 콘텐츠만
    - `border-box` (권장): width/height = 콘텐츠 + padding + border

### 주요 개념

- **Flexbox**
    - 
    
    **Flexbox**는 1차원 레이아웃을 위한 배치 방식입니다.
    
    **기본 사용법**
    
    ```css
    .container {
      display: flex;
      justify-content: center;  /* 가로 정렬 */
      align-items: center;      /* 세로 정렬 */
      gap: 10px;                /* 아이템 간격 */
    }
    
    ```
    
    **컨테이너 속성 (Container)**
    
    | 속성 | 값 | 설명 |
    | --- | --- | --- |
    | `flex-direction` | row, column | 배치 방향 |
    | `justify-content` | flex-start, center, space-between | 기본축 정렬 |
    | `align-items` | flex-start, center, stretch | 교차축 정렬 |
    | `flex-wrap` | nowrap, wrap | 줄바꾼 여부 |
    | `gap` | px, rem | 아이템 간격 |
    
    **아이템 속성 (Item)**
    
    | 속성 | 설명 | 예시 |
    | --- | --- | --- |
    | `flex-grow` | 늘어나는 비율 | `flex-grow: 1;` |
    | `flex-shrink` | 줄어드는 비율 | `flex-shrink: 0;` |
    | `flex-basis` | 기본 크기 | `flex-basis: 200px;` |
    | `align-self` | 개별 정렬 | `align-self: flex-end;` |
- **Grid**
    - 
    
    **Grid**는 2차원 레이아웃을 위한 배치 방식입니다.
    
    **기본 사용법**
    
    ```css
    .container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);  /* 3열 균등 분할 */
      grid-template-rows: auto;
      gap: 20px;
    }
    
    ```
    
    **컨테이너 속성**
    
    | 속성 | 설명 | 예시 |
    | --- | --- | --- |
    | `grid-template-columns` | 열 정의 | `repeat(3, 1fr)` |
    | `grid-template-rows` | 행 정의 | `100px auto 100px` |
    | `gap` | 격자 간격 | `gap: 20px;` |
    | `justify-items` | 셀 내 가로 정렬 | `center` |
    | `align-items` | 셀 내 세로 정렬 | `center` |
    
    **아이템 속성**
    
    | 속성 | 설명 | 예시 |
    | --- | --- | --- |
    | `grid-column` | 열 위치/범위 | `grid-column: 1 / 3;` |
    | `grid-row` | 행 위치/범위 | `grid-row: 1 / 2;` |
    | `grid-area` | 영역 지정 | `grid-area: header;` |


**CSS 애니메이션**으로 동적인 효과를 적용할 수 있습니다.

**Transition (전환 효과)**

```css
.button {
  background: #3498db;
  transition: all 0.3s ease;
}
.button:hover {
  background: #2980b9;
  transform: scale(1.1);
}

```

**Transition 속성**

| 속성 | 설명 | 예시 |
| --- | --- | --- |
| `transition-property` | 적용 속성 | `all`, `background` |
| `transition-duration` | 지속 시간 | `0.3s`, `500ms` |
| `transition-timing-function` | 가속도 | `ease`, `linear` |
| `transition-delay` | 지연 시간 | `0.1s` |

**Animation (키프레임)**

```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.element {
  animation: fadeIn 1s ease-in-out;
}

```

**Transform 속성**

| 함수 | 설명 | 예시 |
| --- | --- | --- |
| `translate()` | 이동 | `translateX(50px)` |
| `rotate()` | 회전 | `rotate(45deg)` |
| `scale()` | 확대/축소 | `scale(1.5)` |
| `skew()` | 기울임 | `skewX(10deg)` |
