# 시리즈 게시글 조회

## SelectSereisPosts - 시리즈 게시글 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/lolog/{user_id}/series/{series_id}

### Parameter

**parma**

- user_id : 롤로그 소유자의 ID
- series_id : 조회하고자 하는 시리즈의 ID

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> 시리즈 게시글 조회 성공

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "series": [
    {
      "post_series_sort": 1,
      "post_title": "제목",
      "post_content": "내용",
      "post_thumbnail": "",
      "post_create_at": "2022-11-23T06:39:01.544Z",
      "series_id": 2,
      "user_id": 1,
      "post_id": 11
    },
    {
      "post_series_sort": 2,
      "post_title": "게시글제목",
      "post_content": "내용",
      "post_thumbnail": "",
      "post_create_at": "2022-11-29T04:34:05.935Z",
      "series_id": 2,
      "user_id": 1,
      "post_id": 59
    },
    ....
  ]
}
```

- post_series_sort : 시리즈에 설정된 게시글의 정렬 순서
- post_title : 게시글의 제목
- post_content : 게시글의 내용
- post_thumbnail : 게시글의 썸네일
- post_create_at : 게시글 작성일
- series_id : 해당 시리즈의 ID
- user_id : 시리즈를 생성한 사용자의 ID
- post_id : 게시글의 ID

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> 시리즈 게시글 조회 실패
