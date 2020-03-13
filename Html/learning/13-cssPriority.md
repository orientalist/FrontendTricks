# css權重
1. 指定html標籤為1分
2. 指定class為10分(可累加)
3. 指定id/為100分
4. 行內樣式為1000分
5. 最終套用分數高者(同分/同標籤套用後者)
6. `!important`為10000分
```css
1分
h1{
    color:red;
}
11分
.header h1{
    color:blue;
}
21分
.header .left h1{
    color:yellow;
}
100分
#title{
    color:green;
}
```