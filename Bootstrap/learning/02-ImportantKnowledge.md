# 重要的整體樣式
## Html5文件類型
Bootstrap 要求使用 HTML5 文件類型。沒有這個文件類型，你會看見一些奇怪的不完整格式。但加入這個文件類型應當不會導致任何錯誤。
```html
<!doctype html>
<html lang='en'>
...
</html>
```
***
## 響應式meta tag
Bootstrap 的開發以 行動優先 為策略，按照這個策略，我們優先為行動裝置優化程式碼，然後使用 CSS media queries 在必要時放大元件。為了確保全部裝置上有正確渲染和和觸控縮放，將響應式中繼標籤記 添加到你的`<head>`中。
```html
<meta name='viewport' content='width=device-width, initial-scale=1, shrink-to-fit=no'>
```
***
## Box-sizing
為了在 CSS 中能夠更加直接的調整尺寸，我們將整體的 box-sizing 數值從 content-box 切換為 border-box。這就確保了 padding 不會影響元素最終的計算寬度，但這可能導致在 Google 地圖和 Google 自訂搜尋引擎等某些第三方元件出現問題。

在極少的情形中，你需要使用類似於如下的設置：
```css
.selector-for-some-widget {
  box-sizing: content-box;
}
```
***
## 重置(Reboot)
針對單一檔案內 CSS 的`特定元素`重置樣式，重置以便 Bootstrap 準確且一致的建立樣式。
換言之,為了使Bootstrap樣式能正確運作,以bootstrap的標準樣式套用至所有使用bootstrap樣式的頁面。
### 方式
僅針對 HTML 語法與元素語法重置並建立規範。附加樣式僅能利用 class 建立。例如，我們利用重置部分 <table> 基礎樣式以利套用後續的 .table、.table-bordered 及其他選項。

以下是我們重置元件的規範和原因：

- 更新部分瀏覽器的預設值，在可變動的文字間距上使用 rems 替代 ems。
- 避免 margin-top。垂直邊緣可能會發生重疊，產生無法預料的錯誤。更重要的是 margin 應該是單向、簡單的思維。
- 為了在設備之間之間輕鬆縮放，方塊元素應當在 margin 上採用 rem。
- 盡可能使用 inherit 將字體的屬性宣告保持在最小化。

### 頁面預設
為了提供最佳的頁面預設值而更新`<html>` 和 `<body>` 元素。具體而言：

- 在每個元素上設定全域性的 box-sizing，包括 *::before 和 *::after 以及 border-box。這確保元素物件 padding 或 border 不會超過宣告的寬度數值。
不在 `<html>` 上宣告基礎 font-size，但假設字體尺寸為 16px (瀏覽器預設)。font-size: 在 `<body>` 上應用 1rem 以便於透過 media queries 時採用使用者的喜好與設定輕易設定響應式縮放。
- `<body>` 同時設定一個全域的 font-family 和 line-height 及 text-align，隨後某些元素形式會繼承這個設定以防止字體不一致。
- 安全起見在 `<body>` 宣告 background-color 預設值為 #fff。

### 原生字體堆疊
Bootstrap 4.0 已經放棄了預設網頁字體（Helvetica Neue, Helvetica, 和 Arial）並用 “native font stack” 取代了預設字體以在每個設備和作業系統上獲得最佳的閱讀呈現。
```css
$font-family-sans-serif:
  // Safari for OS X and iOS (San Francisco)
  -apple-system,
  // Chrome < 56 for OS X (San Francisco)
  BlinkMacSystemFont,
  // Windows
  "Segoe UI",
  // Android
  "Roboto",
  // Basic web fallback
  "Helvetica Neue", Arial, sans-serif,
  // Emoji fonts
  "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol" !default;
```
`<body>` 應用 font-family 並在整個 Bootstrap 內自動繼承這個全域設定。要切換全域的 font-family，更新 $font-family-base 並重新編譯 Bootstrap。

### 標題和段落
所有標題元素像是 `<h1>` 及 `<p>` 已經刪除它們的 margin-top。標題元素具有 margin-bottom: .5rem，段落元素則是 margin-bottom: 1rem 使其具有更單純的間隔。

[完整重置項目](https://bootstrap.hexschool.com/docs/4.1/content/reboot/)
***