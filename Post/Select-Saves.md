# 임시글 조회

## SavesPostList - 임시글 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/posts/saves

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> 임시글 조회 성공

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "post": [
    {
      "post_title": "임시글 제목",
      "post_content": "임시글 내용",
      "post_status": 3,
      "post_thumbnail": "",
      "post_likes": 0,
      "post_comment_count": 0,
      "post_create_at": "2022-11-18T13:53:47.515Z",
      "user_id": 1,
      "post_id": 4,
      "tags": null
    }
  ]
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> 임시글 조회 실패
