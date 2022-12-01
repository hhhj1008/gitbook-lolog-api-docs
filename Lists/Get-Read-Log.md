# 최근 읽은 게시글 목록

## GetReadList - 최근 읽은 게시글 목록

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/lists/read

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
