# 프로필 이미지 수정

## UpdateProfileImage - 프로필 이미지 수정

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/users/profile_image

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "profile_image": "profile_image"
}
```

- profile_image: 빈 값이면 이미지 삭제

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> update profile image success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "update profile image success",
  "data": {
    "profile_image": "profile_image"
  }
}
```

</div>
</details>
