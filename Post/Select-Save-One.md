# 임시글 조회

## SelectSaveOne - 임시글 조회

![](https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET) http://localhost:8000/posts/saves/{post_id}

### Parameter

**parma**

- post_id : 조회할 임시글의 ID

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200) 임시글 조회 성공

<details>

<summary>결과 값</summary>

```json
{
  "statusCode": 200,
  "post": [
    {
      "post_id": 265,
      "user_id": 3,
      "title": "게시글 제목",
      "content": "게시글 내용",
      "tags": [
        {
          "tag_id": 1,
          "tag_name": "태그1"
        },
        {
          "tag_id": 2,
          "tag_name": "태그2"
        }
      ]
    }
  ]
}
```

</details>
