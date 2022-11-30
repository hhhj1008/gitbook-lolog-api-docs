# 썸네일

## ThumbnailUpload - 썸네일 업로드

![](https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST) http://localhost:8000/uploads/thumbnail?image_url={image_url}

### Parameter

**query**

- image_url : 썸네일을 재업로드 할 경우 기존 imageURL을 필요로 함.

**body - form-data**

- key : image / value: image_file

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200) thumbnail upload success

<details>

<summary>결과 값</summary>

```json
{
  "statusCode": 200,
  "imageUrl": "http://localhost:8000/public/5b6aab81-f70a-4b21-be3e-adc948fbe3f7.jpg"
}
```

</details>

![](https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403) thumbnail upload failed

## ThumbnailDelete - 썸네일 삭제

![](https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE) http://localhost:8000/uploads/thumbnail?image_url={image_url}

### Parameter

**query**

- image_url : 삭제할 이미지의 URL.

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200) thumbnail delete success

![](https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403) thumbnail delete failed
