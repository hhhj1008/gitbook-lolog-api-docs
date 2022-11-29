# 댓글 수정

## UpdateCommnet - 댓글 수정

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/comments/{post_id}/{comment_id}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**parma**

- post_id : 댓글이 포함된 게시글의 ID
- comment_id : 수정할 댓글의 ID

**body - json**

```json
{
  "content": "수정할 댓글 내용"
}
```

- content : 필수로 작성

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> comment update success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json

```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> comment update failed
