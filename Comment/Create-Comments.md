# 댓글 작성

## CreateCommnet - 댓글 작성

![](https://img.shields.io/badge/POST-green?style=plastic\&logo=appveyor\&logo=POST) http://localhost:8000/comments/{post\_id}

### Parameter

**authorization - Bearer Token**

* login 시 발급 받은 access token

**parma**

* post\_id : 댓글을 작성하고자 하는 게시글의 ID

**body - json**

```json
{
  "content": "댓글 내용",
  "parent_id": 1
}
```

* content : 필수로 작성
* parent\_id : 대댓글이 작성될 상위 댓글의 ID.&#x20;

### Responses

![](https://img.shields.io/badge/201-519800?style=plastic\&logo=appveyor\&logo=201) comment create success

<details>

<summary>결과 값</summary>

```json
```

</details>

\


![](https://img.shields.io/badge/403-DB3A00?style=plastic\&logo=appveyor\&logo=403) comment create failed
