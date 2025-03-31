
## CSV檔案讀取

請使用pandas讀取以下URL中的CSV檔案

1. 顯示前5筆資料
2. 取出“測站名稱”、“縣市”、“空氣品質指標”、“經度”、“緯度”欄位

```python
import pandas as pd
url = "https://data.moenv.gov.tw/api/v2/aqx_p_432?api_key=58d6040c-dca7-407f-a244-d0bfdfa8144a&limit=1000&sort=ImportDate%20desc&format=CSV"
# pd.read_csv()
```

## 爬蟲 or 文字讀取

請試著將https://www.theguardian.com/us-news/2025/mar/30/donald-trump-angry-vladimir-putin-ukraine-nbc
此新聞網站的本文部分擷取出來，並統計檔案中出現次數最多的單字及其出現次數。
並排除stop words https://www.geeksforgeeks.org/removing-stop-words-nltk-python/

