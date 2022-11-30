# 소개글 조회

## SelectAbout - 소개글 조회

![](https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET) http://localhost:8000/lolog/{user_id}/about

### Parameter

**parma**

- user_id : 롤로그 소유자의 ID

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200) 소개글 조회

<details>

<summary>결과 값</summary>

```json
{
  "statusCode": 200,
  "about": {
    "user_id": 1,
    "about_blog": "소개글"
  }
}
```

</details>

![](https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403) 소개글 조회 실패
