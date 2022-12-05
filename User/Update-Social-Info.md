# 소셜 정보 수정

## UpdateUser - 소셜 정보 수정

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/users?type=social_info

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "social_info_email": "updated_social_info_email@test.com",
  "social_info_github": "updated_github_url",
  "social_info_twitter": "updated_twitter_url",
  "social_info_facebook": "updated_facebook_url",
  "social_info_url": "www.updatedUserInfoUrl.com"
}
```

- social_info_email: email 형식
- social_info_url: url 형식
- 없으면 빈 값으로 변경

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> update user success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "update user success",
  "data": {
    "social_info_email": "updated_social_info_email@test.com",
    "social_info_facebook": "updated_facebook_url",
    "social_info_twitter": "updated_twitter_url",
    "social_info_github": "updated_github_url",
    "social_info_url": "www.updatedUserInfoUrl.com"
  }
}
```

</div>
</details>
