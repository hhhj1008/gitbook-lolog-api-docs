# 내가 팔로우한 사람이 작성한 게시글

## GetFolloweePosts - 내가 팔로우한 사람이 작성한 게시글

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/users/follow/post

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
    "posts": [
        {
            "user_login_id": "josephscahn1",
            "user_profile_image": null,
            "post_title": "4번",
            "post_content": "4번",
            "post_thumbnail": "4번",
            "post_comment_count": 0,
            "post_create_at": "2022-11-28T07:35:39.754Z",
            "user_id": 1,
            "post_id": 4,
            "tags": [
                {
                    "tag_id": 1,
                    "tag_name": "javascript"
                },
                {
                    "tag_id": 3,
                    "tag_name": "helloWorld"
                }
            ]
        },
        ...
    ]
}
```

</div>
</details>
