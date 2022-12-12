# 시리즈 조회

## getSeries - 시리즈 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/series/{user_id}

### Parameter

**parma**

- user_id : 조회할 시리즈 소유자의 ID

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
