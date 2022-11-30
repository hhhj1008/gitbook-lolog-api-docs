# 시리즈 생성

## createSeries - 시리즈 생성

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/series

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "series_name": "시리즈 이름"
}
```

- series_name : 생성하고자 하는 시리즈의 이름. 필수 값

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> series create success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 201,
  "series": [
    {
      "series_series_name": "시리즈 이름",
      "series_post_count": 0,
      "series_create_at": "2022-11-24T11:10:08.272Z",
      "series_thumbnail": "",
      "series_id": 1
    }
  ]
}
```

- series_thumbnail : 시리즈의 썸네일
- series_series_name : 시리즈의 이름
- series_post_count : 시리즈에 포함된 게시글의 수
- series_create_at : 시리즈가 생성된 일자
- series_id : 생성된 시리즈의 ID

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> series create failed
