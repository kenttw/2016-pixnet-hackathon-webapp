## 時尚、美妝部落客及文章資料說明
這份資料包裡，包含了「部落格清單」、「影響力百大部落客」、「最新文章內容」三種類型的資料可供運用。

### 部落格清單
整理了部落格全站分類為 `時尚美妝` 的的部落格清單，並篩選點閱數前一萬名作為這份資料。
 
#### 資料細部
```json
{
    "username": "使用者名稱",
    "nickname": "使用者暱稱",
    "blog": {
        "name": "部落格名稱",
        "url": "部落格網址",
        "hit": "累積部落格人氣",
        "comments_count": "累積留言數",
        "articles_count": "總發表文章數",
        "description": " 部落格描述",
        "category": "部落格所屬分類ID",
        "rank": {
            "all": "全站部落格排名",
            "category": "分類部落格排名"
        }
    },
    "usage_days": "使用痞客邦天數",
    "subscriber_count": "訂閱數",
    "friend_count": "好友數"
}
```


### 影響力百大部落客
參考痞客邦社群影響力網站，分別依據「人氣力」、「擴散力」、「搜尋力」，分別挑選出前100大影響力部落客。因此在這份資料中，可以看到populous_power(人氣力)、search_power(搜尋力)、spread_power(搜尋力)三個JSON檔案，排名相關說明可參考痞客邦社群影響力網站。

#### 資料細部
```json
{
    "username": "使用者名稱",
    "nickname": "使用者暱稱",
    "blog": {
        "category": "部落格所屬分類ID",
        "url": "部落格網址",
        "name": "部落格名稱",
    },
    "rank": "影響力排名"
}
```

### 最新文章內容
整理2013年以來，全章文章分類為 `時尚流行`、`美容彩妝`兩個類別的優質文章，共整理約100,000篇。

#### 資料細部
```json
{
    "username": "使用者名稱",
    "url": "文章網址",
    "title": "文章標題",
    "content":"文章內容",
    "blog-name":"部落格名稱",
    "blog-id":"文章編號",
    "blog-category":"部落格全站分類",
    "date":"文章發表日期",
    "hits":"文章點擊數"
}
```

### 相關說明
- 部落格全站分類 - https://developer.pixnet.pro/#!/doc/pixnetApi/blogSiteCategories
- 部落格文章全站分類 - https://developer.pixnet.pro/#!/doc/pixnetApi/mainpageBlogCategories
- 痞客邦社群影響力網站 - https://blogranking.events.pixnet.net/
