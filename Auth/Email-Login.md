# 이메일 로그인

## Login - 이메일 로그인

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/auth/login

### Parameter

**body - json**

```json
{
  "login_id": "josephscahn2",
  "password": "josephscahn2"
}
```

<br>

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/>

<details>
<summary>결과값</summary>
<div markdown="1">

```json
{
  "message": "login success",
  "token": "토큰 값"
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> 
<details>
<summary>결과값 - 로그인 아이디 틀림</summary>
<div markdown="1">

```json
{
  "statusCode": 403,
  "message": "로그인 아이디를 확인 해주세요",
  "error": "Forbidden"
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/401-DB3A00?style=plastic&logo=appveyor&logo=401"/> 
<details>
<summary>결과값 - 비밀번호 불일치</summary>
<div markdown="1">

```json
{
  "statusCode": 401,
  "message": "Unauthorized"
}
```

</div>
</details>
