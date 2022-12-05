# 이메일 중복 확인 및 인증번호 전송

## CheckEmail - 이메일 중복 확인 및 인증번호 전송

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/auth/email

### Parameter

**body - json**

```json
{
  "email": "이메일 주소"
}
```

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "Send Email",
  "signup_code": "0073"
}
```

- signup_code : 0000 ~ 9999 사이의 정수
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
  "message": "이미 가입된 이메일입니다."
}
```

</div>
</details>
