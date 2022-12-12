# 시리즈 조회

## selectSeriesList - 시리즈 조회

게시글 작성 / 수정 시 [시리즈에 추가하기] 버튼을 클릭하였을 때의 API

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/series

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> 시리즈 조회 성공

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "series": [
    {
      "series_series_name": "시리즈 이름1",
      "series_thumbnail": null,
      "series_post_count": 0,
      "series_update_at": "2022-12-01T12:13:42.632Z",
      "series_id": 9
    },
    {
      "series_series_name": "시리즈 이름2",
      "series_thumbnail": null,
      "series_post_count": 1,
      "series_update_at": "2022-12-05T06:38:24.723Z",
      "series_id": 10
    }
  ]
}
```

- series_series_name : 시리즈의 이름
- series_thumbnail : 시리즈의 썸네일.
- series_post_count : 시리즈에 포함된 게시글의 수
- series_create_at : 시리즈의 수정일자
- series_id : 시리즈의 ID

</div>
</details>

<br>
