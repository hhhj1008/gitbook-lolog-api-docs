# 게시글 상세 페이지 조회

## SelectPostDetail - 게시글 상세페이지 조회

![](https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET) http://localhost:8000/lolog/{user_id}/{post_id}

### Parameter

**parma**

- user_id : 롤로그 소유자의 ID
- post_id : 댓글을 작성하고자 하는 게시글의 ID

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200) 게시글 상세페이지 조회 성공

<details>

<summary>결과 값</summary>

```json
   {
    "statusCode": 200,
    "series": [
        {
            "sort": 1,
            "id": 11,
            "title": "제목"
        },
        {
            "sort": 1,
            "id": 59,
            "title": "제목"
        }
    ],
    "post": {
        "user_id": 1,
        "login_id": "게시글 작성자의 login_id",
        "name": "게시글 작성자의 name",
        "profile_image": null,
        "about_me": "게시글 작성자의 한줄 소개",
        "post_id": 8,
        "title": "제목",
        "status": 1,
        "content": "내용",
        "create_at": "2022-11-29T08:56:51.998Z",
        "likes": 1,
        "tags": [
            {
                "tag_id": 1,
                "tag_name": "태그"
            }
        ],
        "comment_count": 11,
        "is_writer": "1",
        "is_follower": "1",
        "is_liked": "0",
    },
    "next_post": {
        "post_id": 9,
        "title": "다음 포스트"
    },
    "pre_post": {
        "post_id": 7,
        "title": "이전 포스트"
    },
    "comments": [
        {
            "post_id": 8,
            "user_id": 1,
            "comment_login_id": "댓글 작성자의 login_id",
            "comment_profile_image": null,
            "comment_id": 9,
            "content": "댓글 내용",
            "create_at": "2022-11-21T05:21:52.135Z",
            "nested_comments": [
                {
                    "comment_id": 10,
                    "content": "대댓글 1",
                    "user_id": 1,
                    "comment_login_id": "댓글 작성자의 login_id",
                    "create_at": "2022-11-21 14:27:16.393231",
                    "is_comments_writer": 1,
                    "comment_profile_image": null
                },
                {
                    "comment_id": 11,
                    "content": "대댓글 2",
                    "user_id": 1,
                    "comment_login_id": "댓글 작성자의 login_id",
                    "create_at": "2022-11-21 14:27:16.393231",
                    "is_comments_writer": 1,
                    "comment_profile_image": null
                },
            ],
            "is_comments_writer": 1
        },
    ],
    "interested": [
        {
            "post_title": "제목",
            "post_content": "내용",
            "post_thumbnail": "",
            "post_views": 3,
            "post_likes": 0,
            "post_comment_count": 0,
            "create_at": "2022-11-18T13:54:37.144Z",
            "user_login_id": "게시글 작성자의 login_id",
            "user_profile_image": null,
            "user_id": 1,
            "post_id": 5
        },
        {
            "post_title": "제목",
            "post_content": "내용",
            "post_thumbnail": "",
            "post_views": 0,
            "post_likes": 0,
            "post_comment_count": 0,
            "create_at": "2022-11-29T07:19:04.915Z",
            "user_login_id": "게시글 작성자의 login_id",
            "user_profile_image": null,
            "user_id": 3,
            "post_id": 60
        },
        ......
    ]
}
```

- series : 설정된 시리즈의 게시글 목록
- post : 게시글의 상세 페이지 내용. is_writer가 1일 땐 로그인한 사용자와, 작성자가 일치. 0일 경우엔 불일치
- next_post : 다음 게시글 정보
- pre_post : 이전 게시글 정보
- comments : 게시글에 작성된 댓글들의 목록. is_comments_writer 가 1일 땐 로그인한 사용자와, 작성자가 일치. 0일 경우엔 불일치.
- interested : 관심 있을 만한 포스트들의 목록.

</details>

![](https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403) 게시글 조회 실패
