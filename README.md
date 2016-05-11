# 2016_pixnet_hackathon_webapp

## 資料說明

- 所有資料皆以 ZIP 格式壓縮
- JSON 格式請參考 http://json.org/
- GeoJSON 格式請參考 http://geojson.org/
- 相簿、部落格分類的ID對應
  - 相簿分類 https://developer.pixnet.pro/#!/doc/pixnetApi/mainpageAlbumCategories
  - 文章分類 https://developer.pixnet.pro/#!/doc/pixnetApi/mainpageBlogCategories
  - 部落格分類 https://developer.pixnet.pro/#!/doc/pixnetApi/blogSiteCategories

## 資料集類型

- ***PIXNET Open API***
- ***分類熱門照片***
- ***美妝人氣熱門部落客文章***



## PIXNET Open API

所有公開資料不需要認證即可存取；而要操作私人資訊（例如發表文章）則需要使用 OAuth 做認證，你可以透過報名時填寫的 API Key 存取 PIXNET API 而不受存取次數限制，至於 API 可到開發網站上申請。

API鏈結 : https://developer.pixnet.pro/

## 分類熱門照片

各分類前10,000張熱門點閱照片的相關資料，以使用者權限設定「完全公開」，並含有***EXIF***與***位置***資料為限。

- 提供***色碼***資訊，為顏色佔圖片比例，提供前 64 色。

資料格式：

ZIP 檔案內有 24 個 JSON 檔案，檔案名稱為 ***相簿分類 ID***，分類名稱請參考頁面上方「資料使用須知」。所有的資料一定有 EXIF 與位置資訊。而檔案內文則是 10,000 筆 JSON 資料，每一筆 JSON 即為一張熱門照片的相關資訊。

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

國內外旅遊、美食記錄、藝文生活、攝影寫真等地理位置相關文章分類的熱門地點



## 資料使用須知











