# 좋아요

## Like - 좋아요

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/posts/{post_id}/like

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**param**

- post_id : 게시글의 ID

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 201
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/409-DB3A00?style=plastic&logo=appveyor&logo=409"/> 
<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 409,
  "message": "이미 좋아요를 한 게시글 입니다"
}
```

</div>
</details>
