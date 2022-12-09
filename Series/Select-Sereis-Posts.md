# 시리즈 게시글 조회

## SelectSereisPosts - 시리즈 게시글 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/series/posts/{series_id}?sort=asc

### Parameter

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
      "series_thumbnail": "",
      "post_series_sort": 1,
      "post_title": "게시글 제목",
      "post_content": "게시글 내용",
      "post_create_at": "2022-12-07T07:15:55.290Z",
      "series_id": 13,
      "user_id": 3,
      "post_id": 105,
      "is_owner": 0
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

<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> BadRequestException

<details>

<summary>오류 내용</summary>

```json
{
  "statusCode": 400,
  "message": "...."
}
```

- query의 sort가 없거나, asc/desc 이 외의 값을 보냈을 경우

</details>
