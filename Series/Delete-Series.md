# 시리즈 삭제

## deleteSeries - 시리즈 삭제

<img src="https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE"/> http://localhost:8000/series/{series_id}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**query**

- series_id : 삭제하려는 시리즈의 ID

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> delete seires success

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> delete seires failed
