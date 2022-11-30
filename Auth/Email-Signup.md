# 이메일 회원가입

## Signup - 이메일 회원가입

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/auth/signup?type=email

### Parameter

**body - json**

```json
{
  "email": "이메일",
  "name": "이름",
  "password": "비밀번호",
  "login_id": "로그인 아이디",
  "about_me": "나에 대한 소개"
}
```

- email: email 형식, 필수
- name: 20자 이하, 필수
- password: 8~16자, 필수
- login_id: 15자 이하, 필수
- about_me: 선택

<br>

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/>

<details>
<summary>결과값</summary>
<div markdown="1">

```json
{
  "message": "signup & login success",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7InN1YiI6NywibG9naW5faWQiOiJhaG5zdWNoZW8yIiwibmFtZSI6IuyViOyImOyyoCJ9LCJpYXQiOjE2Njk4MDg1Nzd9.PpSfdWxjeKO35m5TVX4_3g1HxWeqBU7_W0YwG72Hp4A"
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/409-DB3A00?style=plastic&logo=appveyor&logo=409"/> 
<details>
<summary>결과값 - 이메일 중복</summary>
<div markdown="1">

```json
{
  "statusCode": 409,
  "message": "이메일이 중복 되었습니다",
  "error": "Conflict"
}
```

</div>
</details>
