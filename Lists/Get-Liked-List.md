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
{
  "LIKED_POST": [
    {
      "title": "4번",
      "content": "4번",
      "post_id": 4,
      "user_id": 1,
      "create_at": "2022년 11월 28일",
      "thumbnail": "4번",
      "user_name": "안수철1",
      "post_likes": 1,
      "post_comment_count": 0,
      "user_profile_image": null
    },
    ...
  ]
}
```

</div>
</details>
