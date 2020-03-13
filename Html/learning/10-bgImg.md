# background-image
1. 使用時機:某元素(如:div)內有其他元素/文字,而需要背景(使用img無法在內填充元素/文字)
2. `repeat`:該屬性可設定背景圖重複方式,有`no-repeat`,`repeat-x`,`repeat-y`,用以朝x或y方向填充同一圖片,達到節省網頁大小的目的
3. 與`background-color`混用:單一背景圖當元素內容向下延伸超過元素高度時,雖會在y軸向下繼續重複,但視覺效果差,可透過設定`background-color`填充背景圖片被內容超過的部分**不可設定背景圖片repeat-y**