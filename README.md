<center><h1> Mobile App / Web App 應用設計 </h1></center>
----
痞客邦擁有大量優質的原創內容，除了一直以來受到大眾熟悉喜愛的吃、喝、玩、樂主題分享。今年，我們特地加入豐富的時尚、美妝精彩元素，讓參賽者擁有更多創新的發想空間。

### 資料說明
----
* 分類熱門照片
  * 資料簡介：全站相簿內容分類涵蓋極廣，譬如：國內外旅遊、美食紀錄、親子、攝影...等，這份資料包含各分類的熱門照片詳細資料，以使用者權限設定「完全公開」為前提，並且含有 EXIF 以及位置(經緯度)資料為限。（提供照片***色碼***資訊，為顏色佔圖片比例，提供前 64 色。）
  * 資料範圍：包含24個分類，約18萬筆資料。
  * [資料細部](./01_hot_picture/01_data_schema.md)
  * [資料範例](./01_hot_picture/01_sample.json)
  * [下載完整資料集](http://www.pixnet.net)
* 時尚、美妝部落客及文章
  * 資料簡介：時尚、美妝相關內容近來在痞客邦有蓬勃發展的趨勢，此資料集中，整理了包含時尚美妝類的：「部落格清單」、「最新文章內容」、「影響力百大部落客」，此外還可搭配分類熱門照片中的時尚美妝類照片，做出各種搭配應用。
  * 資料範圍：約4萬多個部落格，篇精選文章，以及影響力百大部落客名單。
  * [資料細部](./02_fashion_and_beauty/02_data_schema.md)
  * [資料範例1](./02_fashion_and_beauty/02_article_sample.json)、[資料範例2](./02_fashion_and_beauty/02_blog_list_sample.json)、[資料範例3](./02_fashion_and_beauty/02_top_author_sample.json)
  * [下載完整資料集](http://www.pixnet.net)
* 分類熱門地點相關文章
  * 資料簡介：選取全站15個與地理位置較相關的分類(ex.  美食, 活動, 親子...等)，擷取各分的熱門地點所對應的相關文章。
  * 資料範圍：包含15個分類，約10萬筆文章內容及相關資料。
  * [資料細部](./03_hot_location_article/03_data_schema.md)
  * [資料範例](./03_hot_location_article/03_sample.json)
  * [下載完整資料集](http://www.pixnet.net)
* PIXNET Open API
  * 資料簡介：所有公開資料不需要認證即可存取；而要操作私人資訊（例如發表文章）則需要使用 OAuth 做認證，你可以透過報名時填寫的 API Key 存取 PIXNET API 而不受存取次數限制，至於 API 可到開發網站上申請。
  * [API鏈結](https://developer.pixnet.pro/)

### 評分標準
---
評分主要跟據三個不同面相，由專業評審做最終判斷。
- 資料利用度：了解資料意涵、充分運用提供資料特性。
- 功能完整性：demo順暢程度、是否有完整的 user story。
- 創新驚艷值：應用能否讓現場觀眾評審驚艷，留下深刻印象及反應。


### 相關參考資料
----
- JSON 格式請參考 http://json.org/
- GeoJSON 格式請參考 http://geojson.org/
- 相簿、部落格分類的ID對應
  - 相簿分類 https://developer.pixnet.pro/#!/doc/pixnetApi/mainpageAlbumCategories
  - 文章分類 https://developer.pixnet.pro/#!/doc/pixnetApi/mainpageBlogCategories
  - 部落格分類 https://developer.pixnet.pro/#!/doc/pixnetApi/blogSiteCategories



