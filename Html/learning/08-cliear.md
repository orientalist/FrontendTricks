# clear
1. float元素為浮動元素,會造成接續其下的元素**不會**以其下方為基點接續
2. 透過`clear`屬性(css)清除浮動8
```html
    <div class='wrap'>
        <div class='content c1'>1</div>
        <div class='content c2'>2</div>
        <div style='clear:both'></div>
        <div class='footer'></div>
    </div>
```