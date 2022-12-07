# 로그인 아이디 중복 확인

## CheckLoginId - 로그인 아이디 중복 확인

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/auth/login_id

### Parameter

**body - json**

```json
{
  "login_id": "로그인 아이디"
}
```

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 201,
  "message": "사용 가능한 로그인 아이디입니다"
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
  "message": "로그인 아이디가 중복되었습니다"
}
```

</div>
</details>
