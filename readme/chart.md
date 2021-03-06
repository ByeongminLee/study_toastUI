# π ToastUI - Chart

[(toastUI-Chart)](http://nhn.github.io/tui.chart/latest/)

[(toastUI-Chart-github)](https://github.com/nhn/tui.chart)

### μ°¨νΈ μ’λ₯

[**Live**](https://byeongminlee.github.io/study_toastUI/page/chart/chart_list.html)

## πΎ μ€μΉ νκΈ°

### npm

```sh
$ npm install --save @toast-ui/chart # μ΅μ  λ²μ 
$ npm install --save @toast-ui/chart@<version> # νΉμ  λ²μ 
```

### CDN

```html
<link rel="stylesheet" href="https://uicdn.toast.com/chart/latest/toastui-chart.min.css" />
<script src="https://uicdn.toast.com/chart/latest/toastui-chart.min.js"></script>
```

### μμ€ νμΌ λ€μ΄λ‘λ

-   [(https://github.com/nhn/tui.chart/releases)](https://github.com/nhn/tui.chart/releases)

<br>

## π μ°¨νΈ μμ±

-   el: μ°¨νΈλ₯Ό μμμμλ‘ κ°λ HTML μμ
-   data: μ°¨νΈμ κΈ°λ°μ΄ λλ μ«μ λ°μ΄ν°
-   options: λ²λ‘, μ λ ¬, ν΄ν ν¬λ§· λ± μ¬λ¬ κΈ°λ₯μ λνλ΄λ μ΅μ

```javascript
const el = document.getElementById("chart-area");
const data = {
    // μΉ΄νκ³ λ¦¬ -> YμΆ
    categories: ["μμΈ", "κ²½κΈ°", "μΈμ²", "μΈμ’", "λΆμ°", "λκ΅¬", "κ΄μ£Ό"],
    // μλ¦¬μ¦ -> name,data νμ κ°
    series: [
        {
            name: "1μ",
            data: [5000, 3000, 5000, 7000, 6000, 4000, 1000],
        },
        {
            name: "2μ",
            data: [3000, 2000, 4000, 5000, 5000, 6000, 2000],
        },
        {
            name: "3μ",
            data: [3000, 4000, 3000, 1000, 2000, 4000, 3000],
        },
    ],
    // μμΈμ΄ 1μμ 5000, 2μμ 3000, 3μμ 3000
};

const options = {
    chart: { title: "μ½λ‘λ νμ§μ", width: 900, height: 400 },
};

const chart = toastui.Chart.barChart({ el, data, options });
```

<br>

![barChart1 κ²°κ³Ό](../readme/img/barChart1.png)

[**barChart1 Live**](https://byeongminlee.github.io/study_toastUI/page/chart/barChart1.html)

<br>

## π οΈ μ΅μ μ€μ 

## stack μ΅μ

```javascript
const options = {
    chart: { title: "μ½λ‘λ νμ§μ", width: 900, height: 400 },
    series: {
        stack: true,
    },
};
```

![barChart2 κ²°κ³Ό](../readme/img/barChart2.png)

[**barChart2 Live**](https://byeongminlee.github.io/study_toastUI/page/chart/barChart2.html)

<br>

<br>

### stack μ΅μμμ μΈλΆ μ΅μ μ€μ 

series.stackμ true == stack.type = 'normal'

```javascript
const options = {
    chart: { title: "μ½λ‘λ νμ§μ", width: 900, height: 400 },
    series: {
        stack: {
            type: "normal",
        },
    },
};
```

<br>

### stack - μ°κ²°μ 

```javascript
const options = {
    chart: { title: "μ½λ‘λ νμ§μ", width: 900, height: 400 },
    series: {
        stack: {
            type: "normal",
            connector: true,
        },
    },
};
```

![barChart3 κ²°κ³Ό](../readme/img/barChart3.png)

[**barChart3 Live**](https://byeongminlee.github.io/study_toastUI/page/chart/barChart3.html)

## selectable μ΅μ

ν΄λΉ series (λ°μ΄ν°) μ νκ°λ₯

```javascript
const options = {
    series: {
        selectable: true,
    },
};
```

### selectable - eventDetectType

| νμ      | μ€λͺ                                                                                                       |
| --------- | ---------------------------------------------------------------------------------------------------------- |
| `point`   | κ°λ³ μλ¦¬μ¦ μμ­μ λ§μ°μ€κ° λ€κ°κ°μΌ νμ§. νμ¬ λ§μ°μ€κ° κ°λ¦¬ν€κ³  μλ ν¬μΈνΈλ₯Ό κΈ°μ€μΌλ‘ λ¨ ν κ°λ§ νμ§λ¨ |
| `grouped` | YμΆμ κΈ°μ€μΌλ‘ κ°μ΄ κ°μ λͺ¨λ  λ°μ΄ν°κ° νμ§λ¨                                                              |

```javascript
const options = {
    chart: { title: "μ½λ‘λ νμ§μ", width: 900, height: 400 },
    series: {
        selectable: {
            eventDetectType: "grouped", // point
        },
    },
};
```

![barChart4 κ²°κ³Ό](../readme/img/barChart4.png)

[**barChart4 Live**](https://byeongminlee.github.io/study_toastUI/page/chart/barChart4.html)
