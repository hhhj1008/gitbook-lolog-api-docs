# 구글 로그인

## GooleAuth - 구글 로그인

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/auth/google

### Parameter

<br>

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/>

<details>
<summary>회원가입이 안된 경우</summary>
<div markdown="1">

```json
{
  "message": "회원가입 먼저 진행해야합니다",
  "user": {
    "provider": "google",
    "providerId": "106270221121024541355",
    "email": "email@email.com",
    "name": "이름",
    "profile_image": "프로필 이미지 링크 ex) https://~~~~.com/~~~"
  }
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> 
<details>
<summary>회원가입을 한 경우</summary>
<div markdown="1">

```json
{
  "message": "Google login success",
  "token": "토큰 값"
}
```

</div>
</details>
