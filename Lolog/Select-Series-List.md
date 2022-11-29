# 시리즈 조회

## SelectSereisPosts - 시리즈 게시글 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/lolog/{user_id}/series

### Parameter

**parma**

- user_id : 롤로그 소유자의 ID

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
      "series_series_name": "시리즈 이름",
      "series_post_count": 1,
      "series_create_at": "2022-11-24T11:10:08.272Z",
      "post_thumbnail": "",
      "series_id": 2
    }
  ]
}
```

- series_series_name : 시리즈의 이름
- series_post_count : 시리즈에 포함된 게시글의 수
- series_create_at : 시리즈의 생성일
- post_thumbnail : 게시글의 썸네일. 정렬 순서가 첫번째로 지정된 게시글의 썸네일을 가지고 옴.
- series_id : 해당 시리즈의 ID

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> 시리즈 조회 실패
