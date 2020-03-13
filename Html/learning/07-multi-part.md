# 多欄式網頁
1. 讓元素**並排**
   1. css:`float`
      - 若並排子元素寬度相加大於父元素,仍會過行
   ```html
    <style>
    .wrap {
        width: 85vw;
        margin: auto;
    }
    .content {
        float: left;
    }
    .c1 {
        background-color: red;
        width: 45vw;
    }
    .c2 {
        background-color: blue;
        width: 40vw;
    }
    </style>
    <div class='wrap'>
        <div class='content c1'>1</div>
        <div class='content c2'>2</div>
    </div>
   ```
