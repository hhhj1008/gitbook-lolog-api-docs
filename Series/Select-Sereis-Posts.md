# 시리즈 게시글 조회

## SelectSereisPosts - 시리즈 게시글 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/series/{series_id}?sort=asc

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**parma**

- series_id : 조회하고자 하는 시리즈의 ID

**query**

- sort : 시리즈의 정렬 순서로 필수로 설정되어야 함. <br> asc(오름차순)/desc(내림차순) 이 외의 값이 들어올 경우 오류 발생.

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
      "series_thumbnail": null,
      "post_series_sort": 1,
      "post_title": "게시글 제목",
      "post_content": "게시글 내용",
      "post_create_at": "2022-11-28T15:30:29.769Z",
      "series_id": 8,
      "user_id": 1,
      "post_id": 53
    },
    {
      "is_owner": 1
    }
  ]
}
```

- series_thumbnail : 시리즈의 썸네일
- post_series_sort : 시리즈에 설정된 게시글의 정렬 순서
- post_title : 게시글의 제목
- post_content : 게시글의 내용
- post_create_at : 게시글 작성일
- series_id : 해당 시리즈의 ID
- user_id : 시리즈를 생성한 사용자의 ID
- post_id : 게시글의 ID
- is_owner : 로그인한 사용자와 시리즈 작성자가 일치할 경우 1 / 일치하지 않으면 0

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> 시리즈 게시글 조회 실패
