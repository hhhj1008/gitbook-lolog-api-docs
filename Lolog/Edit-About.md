# 소개글 편집

## CreatePost - 소개글 편집

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/lolog/{user_id}/about

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**parma**

- user_id : 롤로그 소유자의 ID

**body - json**

```json
{
  "about_blog": "편집할 소개글 내용"
}
```

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> about edit success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "about": {
    "user_id": 1,
    "about_blog": "편집된 소개글의 내용"
  }
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> about edit failed
