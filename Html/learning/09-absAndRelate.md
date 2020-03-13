# 相對/絕對定位
1. 所有元素預設的position屬性值為`static`:不特別定位
2. `position:relative`之元素內的元素可設定`top`,`left`,`right`與`bottom`,該元素便會以父元素左上角為原點移動至指定位置
3. `position:absolute`之元素會向上尋找至第一個非`position:static`之元素,以期為基準移動位置

[參考文章](https://zh-tw.learnlayout.com/position.html)

4. `z-index`:同層元素若重疊,可透過指定`z-index`調整上下關係(預設後元素覆蓋前元素),數值越大者位於上方