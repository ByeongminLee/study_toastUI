# π ToastUI - editor

[(toastUI-Editor-κ°μ΄λ)](https://github.com/nhn/tui.editor/blob/master/docs/ko/README.md)

## πΎ μ€μΉ νκΈ°

### npm

```sh
$ npm install @toast-ui/editor // μ΅μ λ²μ 
$ npm install @toast-ui/editor@<version> // νΉμ λ²μ 
```

### CDN

```html
<link rel="stylesheet" href="https://uicdn.toast.com/editor/latest/toastui-editor.css" />
<script src="https://uicdn.toast.com/editor/latest/toastui-editor-all.min.js"></script>
```

<br>

## μλν° μμ±

```javascript
const Editor = toastui.Editor;

const editor = new Editor({
    el: document.querySelector("#editor"),
});
```

### μ΅μ

-   height: μλν° μμ­μ λκΈ° κ°. λ¬Έμμ΄ κ°μ κ°μ§λ€. 300px | auto

-   initialEditType: μ΅μ΄λ‘ λ³΄μ¬μ€ μλν° νμ. markdown | wysiwyg

-   initialValue: μ½νμΈ  μ΄κΈ°κ°. λ°λμ λ§ν¬λ€μ΄ λ¬Έμμ΄ ννμ¬μΌ νλ€.

-   previewStyle: λ§ν¬λ€μ΄ νλ¦¬λ·° μ€νμΌ. tab | vertical

-   usageStatistics: μλν°λ₯Ό μ¬μ©νλ μΉ μ¬μ΄νΈμ *νΈμ€νΈλͺ*μ μ μ‘νλ€. μ΄λ ν μ¬μ©μκ° μλν°λ₯Ό μ¬μ©νκ³  μλμ§ μμ§νκΈ° μν©λλ€. μ΄ μ΅μμ λΆλ¦¬μΈ κ°μ μ§μ νμ¬ λΉνμ±νν  μ μλ€. true | false
