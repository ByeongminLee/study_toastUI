# 📖 ToastUI - editor

[(toastUI-Editor-가이드)](https://github.com/nhn/tui.editor/blob/master/docs/ko/README.md)

## 💾 설치 하기

### npm

```sh
$ npm install @toast-ui/editor // 최신버전
$ npm install @toast-ui/editor@<version> // 특정버전
```

### CDN

```html
<link rel="stylesheet" href="https://uicdn.toast.com/editor/latest/toastui-editor.css" />
<script src="https://uicdn.toast.com/editor/latest/toastui-editor-all.min.js"></script>
```

<br>

## 에디터 생성

```javascript
const Editor = toastui.Editor;

const editor = new Editor({
    el: document.querySelector("#editor"),
});
```

### 옵션

-   height: 에디터 영역의 높기 값. 문자열 값을 가진다. 300px | auto

-   initialEditType: 최초로 보여줄 에디터 타입. markdown | wysiwyg

-   initialValue: 콘텐츠 초기값. 반드시 마크다운 문자열 형태여야 한다.

-   previewStyle: 마크다운 프리뷰 스타일. tab | vertical

-   usageStatistics: 에디터를 사용하는 웹 사이트의 *호스트명*을 전송한다. 어떠한 사용자가 에디터를 사용하고 있는지 수집하기 위합니다. 이 옵션은 불리언 값을 지정하여 비활성화할 수 있다. true | false
