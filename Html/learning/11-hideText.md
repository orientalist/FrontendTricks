# 將文字隱藏於元素中
1. `text-indent`:文字開頭位置
   1. 設定可為px,%...
2. `overflow`:溢出部分處理
   1. `hidden`:隱藏
3. `white-space`:文字空白處理
   1. `normal`-合併多空白為一,在必要時過行
   2. `nowrap`-合併多空白為一,不過行
   3. `pre`-所有空白保留,僅在過行符號處過行
   4. `pre-line`-合併多空白為一,在必要或過行符號處過行
   5. `pre-wrap`-保留所有空白,在必要或過行符號處過行
4. 隱藏文字
```css
.container{
    將文字開頭推擠至容器外
    text-indent:101%;
    溢出部分隱藏
    overflow:hidden;
    文字不過行
    white-space:nowrap;
}
```