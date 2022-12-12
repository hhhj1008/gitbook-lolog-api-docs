# 좋아요 취소

## Unlike - 좋아요 취소

<img src="https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE"/> http://localhost:8000/posts/{post_id}/like

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**param**

- post_id : 게시글의 ID

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 204
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/404-DB3A00?style=plastic&logo=appveyor&logo=404"/> 
<details>
<summary>(예외처리 예정)결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 404,
  "message": "좋아요를 하지 않은 게시글입니다"
}
```

</div>
</details>
