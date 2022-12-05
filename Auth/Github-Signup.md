# 깃헙 회원가입

## Signup - 깃헙 회원가입

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/auth/signup?type=github

### Parameter

**body - json**

```json
{
  "name": "이름",
  "login_id": "로그인 아이디",
  "about_me": "나에 대한 소개",
  "profile_image": "프로필 이미지"
}
```

- name: 20자 이하, signup에서 넘겨준 데이터 중 name, 필수
- login_id: 15자 이하, 필수
- about_me: 선택
- profile_image: signup에서 넘겨준 데이터 중 profile_image

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

<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> 
<details>
<summary>결과값 - 필수값 누락</summary>
<div markdown="1">

```json
{
  "statusCode": 400,
  "message": [
    "login_id must be longer than or equal to 0 characters",
    "login_id should not be empty"
  ],
  "error": "Bad Request"
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
