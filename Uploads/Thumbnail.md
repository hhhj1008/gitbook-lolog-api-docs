# 썸네일

{% hint style="warning" %}
**API 주소가 변경될 예정입니다.**
{% endhint %}

## ThumbnailUpload - 썸네일 업로드

![](https://img.shields.io/badge/POST-green?style=plastic\&logo=appveyor\&logo=POST) http://localhost:8000/posts/thumbnail

### Parameter

**authorization - Bearer Token**

* login 시 발급 받은 access token

**body - form-data**

* key : image / value: image\_file

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic\&logo=appveyor\&logo=200) thumbnail upload success

<details>

<summary>결과 값</summary>

```json
{
  "statusCode": 200,
  "message": "thumbnail upload success",
  "imageUrl": "http://localhost:8000/public/329f7f7a-3a6f-4365-bf46-45d9ea43c96f.png"
}

```

</details>

![](https://img.shields.io/badge/403-DB3A00?style=plastic\&logo=appveyor\&logo=403) thumbnail upload failed\


## ThumbnailDelete - 썸네일 삭제

![](https://img.shields.io/badge/DELETE-red?style=plastic\&logo=appveyor\&logo=DELETE) http://localhost:8000/posts/thumbnail

### Parameter

**body - json**

```json
{
  "file_name": "3b60ea4a-e73e-4720-8e69-5dc507456fe0.jpg"
}
```

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic\&logo=appveyor\&logo=200) thumbnail delete success

![](https://img.shields.io/badge/403-DB3A00?style=plastic\&logo=appveyor\&logo=403) thumbnail delete failed
