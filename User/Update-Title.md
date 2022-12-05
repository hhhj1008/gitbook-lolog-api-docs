# 제목 수정

## UpdateUser - 제목 수정

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/users?type=title

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "title": "updated_user_title"
}
```

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> update user success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "update user success",
  "data": {
    "title": "updated_user_title"
  }
}
```

</div>
</details>

<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> title must be entered

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 400,
  "message": "title must be entered"
}
```

</div>
</details>
