# 이름 및 소개 수정

## UpdateUser - 이름 및 소개 수정

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/users/type=name

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "name": "updated_user_name",
  "about_me": "updated_about_me"
}
```

- name: 필수값
- about_me: 없으면 빈 값으로 변경

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> update user success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "update user success",
  "data": {
    "name": "updated_user_name",
    "about_me": "updated_about_me"
  }
}
```

</div>
</details>

<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> name must be entered

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 400,
  "message": "name must be entered",
  "error": "Bad Request"
}
```

</div>
</details>
