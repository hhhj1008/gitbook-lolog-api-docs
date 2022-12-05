# 프로필 이미지 수정

## UpdateProfileImage - 프로필 이미지 수정

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/users/profile_image?image_url={image_url}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**query**

- image_url : 프로필 이미지를 재업로드 할 경우 기존 imageURL을 필요로 함.

**body - form-data**

- key : image / value: image_file

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> update profile image success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "update profile image success",
  "profile_image": "http://localhost:8000/public/5b6aab81-f70a-4b21-be3e-adc948fbe3f7.jpg"
}
```

</div>
</details>

<br>
<br>

## DeleteProfileImage - 프로필이미지 삭제

![](https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE) http://localhost:8000/users/profile_image?image_url={image_url}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**query**

- image_url : 삭제할 이미지의 URL.

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200)

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "message": "profile_image delete success"
}
```

</div>
</details>
