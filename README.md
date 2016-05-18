<center><h1> Mobile App / Web App 應用設計 </h1></center>
----
痞客邦擁有大量優質的原創內容，除了一直以來受到大眾熟悉喜愛的吃、喝、玩、樂主題分享。今年，我們特地加入豐富的時尚、美妝精彩元素，讓參賽者擁有更多創新的發想空間。

### 資料說明
* 分類熱門照片
  * 資料簡介：全站相簿內容分類涵蓋極廣，譬如：國內外旅遊、美食紀錄、親子、攝影...等，這份資料包含各分類的熱門照片詳細資料，以使用者權限設定「完全公開」為前提，並且含有 EXIF 以及位置(經緯度)資料為限。（提供照片***色碼***資訊，為顏色佔圖片比例，提供前 64 色。）
  * 資料範圍：包含26個分類，約18萬筆資料。
  * [資料細部](training_data_schema.md)
  * [資料範例](./data/sample_training.json)
  * [下載完整資料集](http://www.pixnet.net)
* 時尚、美妝部落客及文章
  * 資料簡介：時尚、美妝相關內容近來在痞客邦有蓬勃發展的趨勢，此資料集中，整理了包含時尚美妝類的：「部落格清單」、「最新文章內容」、「影響力百大部落客」，此外還可搭配分類熱門照片中的時尚美妝類照片，做出各種搭配應用。
  * 資料範圍：約4萬多個部落格，篇精選文章，以及影響力百大部落客名單。
  * [資料細部](training_data_schema.md)
  * [資料範例](./data/sample_training.json)
  * [下載完整資料集](http://www.pixnet.net)
* 分類熱門地點相關文章
  * 資料簡介：選取全站15個與地理位置較相關的分類(ex.  美食, 活動, 親子...等)，擷取各分的熱門地點所對應的相關文章。
  * 資料範圍：包含15個分類，約10萬筆文章內容及相關資料。
  * [資料細部](training_data_schema.md)
  * [資料範例](./data/sample_training.json)
  * [下載完整資料集](http://www.pixnet.net)
* PIXNET Open API
  * 資料簡介：所有公開資料不需要認證即可存取；而要操作私人資訊（例如發表文章）則需要使用 OAuth 做認證，你可以透過報名時填寫的 API Key 存取 PIXNET API 而不受存取次數限制，至於 API 可到開發網站上申請。
  * [API鏈結](https://developer.pixnet.pro/)


- JSON 格式請參考 http://json.org/
- GeoJSON 格式請參考 http://geojson.org/
- 相簿、部落格分類的ID對應
  - 相簿分類 https://developer.pixnet.pro/#!/doc/pixnetApi/mainpageAlbumCategories
  - 文章分類 https://developer.pixnet.pro/#!/doc/pixnetApi/mainpageBlogCategories
  - 部落格分類 https://developer.pixnet.pro/#!/doc/pixnetApi/blogSiteCategories


- 

資料格式：

ZIP 檔案內有 24 個 JSON 檔案，檔案名稱為 ***相簿分類 ID***，分類名稱請參考頁面上方「資料使用須知」。所有的資料一定有 EXIF 與位置資訊。而檔案內文則是 10,000 筆 JSON 資料，每一筆 JSON 即為一張熱門照片的相關資訊。

資料格式
```json
{
    "id": "照片 ID",
    "title": "照片標題",
    "size": "照片檔案大小，單位為 Bytes",
    "type": "pic",
    "link": "照片頁面網址",
    "url": "照片頁面網址",
    "thumb": "照片小縮圖網址",
    "uploaded_at": "上傳時間 (Unix Timestamp)",
    "hits": {
        "total": "累積總人氣",
    },
    "user": {
        "name": "使用者名稱",
        "display_name": "使用者暱稱",
        "avatar": "使用者頭像",
        "link": "使用者連結",
    },
    "location": {
        "geojson": { // 可參考 http://geojson.org/
            "type": "Point",
            "coordinates": [
                "經度",
                "緯度"
            ]
        }
    },
    "exif": {
        "Camera": "相機型號",
        "ISOSpeedRatings": "ISO值",
        "DateTime": "數位化時間",
        "DateTimeOriginal": "原始數位化時間",
        "DateTaken": "拍攝時間",
        "MeteringMode": "測光模式",
        "Aperture": "光圈",
        "ExposureTime": "快門",
        "FocalLength": "焦距",
        "Latitude": "緯度",
        "Longitude": "經度"
    },
    "tags": [
        "照片標籤"
    ],
    "description": "照片說明",
    "taken_at": "拍照時間",
    "original": "原始大小圖片網址",
    "normal": "中縮圖網址",
    "small_square": "小方型縮圖網址",
    "square": "方形縮圖網址",
    "medium": "中大型縮圖網址",
    "bigger": "大縮圖網址",
    "large": "超大縮圖網址",
    "dimension": {
        "original": {
            "width": "原始圖寬度",
            "height": "原始圖高度"
        },
        "thumb": {
            "width": 90,
            "height": 90
        },
        "small_square": {
            "width": 120,
            "height": 120
        },
        "square": {
            "width": 170,
            "height": 170
        },
        "medium": {
            "width": 450,
            "height": 337
        },
        "normal": {
            "width": 600,
            "height": 450
        }
    },
    "color": {
        "色碼": "顏色佔圖片比例", // 提供前 64 色
    },
    "category" : "分類ID"
}
```



## 美妝人氣熱門部落客文章



## 分類熱門地理位置對應文章

國內外旅遊、美食記錄、藝文生活、攝影寫真等地理位置相關文章分類的熱門地點所對應的文章。檔案名稱為 ***相簿分類 ID***，分類名稱請參考頁面上方「資料使用須知」。檔案內容一行即為一篇熱門地點文章的相關資料，包含網址及經緯度。

資料格式
```json
{
    "url": "文章網址",
    "title": "文章標題",
    "image": "文章首圖網址",
    "latlon": [
        "緯度"
        "經度",
    ]
}
```

資料範例
```json
{
    "url": "http:\/\/tujouan.pixnet.net\/blog\/post\/385983518",
    "title": "[食記] 台北西門 三味食堂。 排兩個小時也甘願的神仙級美味平價生魚片 偷收錄等待排隊時間的神秘好去處  ",
    "image": "http:\/\/pic.pimg.tw\/tujouan\/1408201391-4276459474_n.jpg",
    "latlon": [
        "25.0399169",
        "121.502659"
    ]
}
```




## 資料使用須知











