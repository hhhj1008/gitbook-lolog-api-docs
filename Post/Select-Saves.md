# 임시글 조회

## SavesPostList - 임시글 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/posts/saves

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> 성공

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "saves": [
    {
      "post_id": 4,
      "user_id": 1,
      "title": "제목",
      "content": "내용",
      "create_at": "임시글 저장 일자"
    }
  ]
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/404-DB3A00?style=plastic&logo=appveyor&logo=404"/> NotFoundException

<img src="https://img.shields.io/badge/401-DB3A00?style=plastic&logo=appveyor&logo=401"/> UnauthorizedException

<details>

<summary>오류 내용</summary>

```json
{
  "statusCode": 401,
  "message": "Unauthorized"
}
```

- access token이 없거나 잘못된 access token이 넘어온 경우.

</details>
