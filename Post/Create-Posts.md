# 게시글 작성

## CreatePost - 게시글 작성

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/posts

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
    "title": "게시글 제목",
    "content": "게시글 내용",
    "thumbnail": "썸네일 url",
    "tags": ["태그1", "태그2", ....],
    "series_id": 1,
    "status": 1
}
```

- title & content : 필수로 작성
- thumbnail : 썸네일 업로드 후 반환 되는 imageURL 값 삽입.
- tags : 태그는 선택적으로 입력 가능하며, 여러 개의 태그를 작성할 때는 배열로 작성.
- series_id : 시리즈 ID는 선택적으로 입력 가능하며, 시리즈가 설정된 경우 id값 입력.
- status : 게시글의 상태 값. 1(공개) / 2(비공개) / 3(임시글)

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> post create success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json

```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> post create failed
