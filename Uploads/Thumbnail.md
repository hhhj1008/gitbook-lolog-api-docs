# 썸네일 업로드/삭제

! api 주소 변경할 예정

## ThumbnailUpload - 썸네일 업로드

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/posts/thumbnail

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - form-data**

- key : image / value: image_file

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> thumbnail upload success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "message": "thumbnail upload success",
  "imageUrl": "http://localhost:8000/public/329f7f7a-3a6f-4365-bf46-45d9ea43c96f.png"
}
```

</div>
</details>
<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> thumbnail upload failed

<br>

---

<br>

## ThumbnailDelete - 썸네일 삭제

<img src="https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE"/> http://localhost:8000/posts/thumbnail

### Parameter

**body - json**

```json
{
  "file_name": "3b60ea4a-e73e-4720-8e69-5dc507456fe0.jpg"
}
```

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> thumbnail delete success

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> thumbnail delete failed

<!-- 썸네일은  thumbnail controller로 옮기고 사용자 프로필도 동일한 것 사용하도록 수정.-->
