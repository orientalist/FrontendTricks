# box-sizing
1. css3新增
2. 所有元素該數性質預設為`content-box`(等於原本的寬高計算方法)
3. `border-box`:元素寬高(包含padding與border)等於指定的寬高
4. 直接為所有元素加上該屬性值
```css
*{
    box-sizing:border-box;
}
```
5. prefix(前綴詞)-讓舊瀏覽器可使用該屬性
   1. -moz:firefox
   2. -webkit:chrome
```css
*{
    -moz-box-sizing:border-box;
    -webkit-box-sizing:border-box;
}
```