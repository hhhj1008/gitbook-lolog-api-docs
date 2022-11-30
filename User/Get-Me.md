# 내 정보 불러오기

## GetMe - 내 정보 불러오기

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/users

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "getMe success",
  "user": {
    "followCount": "1",
    "id": 2,
    "profile_image": "profile_image",
    "name": "updated_user_name",
    "about_me": null,
    "title": "josephscahn2.log",
    "email": "josephscahn2@email.com",
    "comment_alert": 1,
    "update_alert": 0,
    "social_info_email": null,
    "social_info_github": null,
    "social_info_twitter": null,
    "social_info_facebook": null,
    "social_info_url": null
  }
}
```

</div>
</details>
