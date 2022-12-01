# 최근 읽은 게시글 삭제

## DeleteReadList - 최근 읽은 게시글 삭제

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/lists/read/{post_id}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**param**

- post_id : 삭제하고자 하는 게시글의 ID

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
    "ReadLog": [
        {
            "post_id": 5,
            "user_id": 3,
            "user_name": "안수철3",
            "post_likes": 0,
            "post_title": "5번",
            "post_content": "5번",
            "post_create_at": "2022년 11월 29일",
            "post_thumbnail": "5번",
            "post_comment_count": 0,
            "user_profile_image": null
        },
        ...
    ]
}
```

</div>
</details>
