# 좋아요한 게시글 목록

## GetLikedList - 최근 읽은 게시글 목록

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/lists/like

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
[
    {
        "post_title": "5번",
        "post_content": "5번",
        "post_thumbnail": "5번",
        "post_likes": 1,
        "post_comment_count": 0,
        "user_name": "hello",
        "user_profile_image": "http://localhost:8000/public/be6313c2-0230-4eef-8c4c-bcb55bc373d6.jpeg",
        "post_id": 5,
        "create_at": "2022-11-29T08:56:44.762Z",
        "user_id": 3
    },
    ...
]
```

</div>
</details>
