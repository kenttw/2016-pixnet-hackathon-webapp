
## 分類熱門照片資料說明

包含24個全站相簿分類，每個JSON檔為一個分類，檔名則分別為：${相簿分類 ID}.json，合計共約18萬筆資料。一筆照片資料即為一行JSON format，行與行之間沒有逗點，僅以換行符號做分隔。

### 詳細資料

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
