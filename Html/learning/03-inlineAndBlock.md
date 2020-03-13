# inline與block
1. block區塊元素-元素寬度等同外容器,僅高度可調整(元素相鄰會過行)
2. inlinec行內元素-元素寬度等同元素內容(元素相鄰不過行)
3. 透過css修改元素為行內或區塊:
```css
div{
    display:inline;
}
a{
    display:block;
}
```