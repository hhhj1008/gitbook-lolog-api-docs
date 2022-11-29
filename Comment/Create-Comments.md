# 댓글 작성

## CreateCommnet - 댓글 작성

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/comments/{post_id}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**parma**

- post_id : 댓글을 작성하고자 하는 게시글의 ID

**body - json**

```json
{
  "content": "댓글 내용",
  "depth": 0,
  "parent_id": 1
}
```

- content : 필수로 작성
- depth : 0 (상위 댓글), 1(대댓글)
- parent_id : 대댓글이 작성될 상위 댓글의 ID. depth가 1일 경우 필수로 작성.

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> comment create success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json

```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> comment create failed
