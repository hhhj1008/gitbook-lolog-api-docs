# 게시글 상세 페이지 조회

## SelectPostDetail - 게시글 상세페이지 조회

![](https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET) http://localhost:8000/posts/{post_id}

### Parameter

**parma**

- post_id : 조회하고자 하는 게시글의 ID

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200) 게시글 상세페이지 조회 성공

<details>

<summary>결과 값</summary>

```json
{
  "statusCode": 200,
  "series": [
    {
      "series_id": 2,
      "series_name": "시리즈 이름",
      "sort": 1,
      "post_id": 103,
      "title": "게시글 제목"
    }
  ],
  "post": {
    "user_id": 3,
    "login_id": "login_id",
    "name": "name",
    "profile_image": "profile_image_uri",
    "about_me": "about_me",
    "post_id": 257,
    "title": "게시글 제목",
    "status": 1,
    "content": "게시글 내용",
    "create_at": "2022-12-09T02:56:15.614Z",
    "comment_count": 0,
    "likes": 0,
    "is_writer": 1,
    "tags": [
      {
        "tag_id": 16,
        "tag_name": "태그1"
      },
      {
        "tag_id": 17,
        "tag_name": "태그2"
      }
    ],
    "post_url": "",
    "description": "",
    "is_follower": 0,
    "is_liked": 0
  },
  "next_post": {
    "post_id": 258,
    "title": "다음 포스트"
  },
  "pre_post": {
    "post_id": 256,
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
      "depth": 0,
      "create_at": "2022-11-21T05:21:52.135Z",
      "nested_comments": [
        {
          "comment_id": 10,
          "depth": 1,
          "content": "대댓글 1",
          "user_id": 1,
          "comment_login_id": "댓글 작성자의 login_id",
          "create_at": "2022-11-21 14:27:16.393231",
          "is_comments_writer": "true",
          "comment_profile_image": null
        }
      ],
      "is_comments_writer": 1
    }
  ],
  "interested": [
    {
      "post_title": "제목1",
      "post_thumbnail": "thumbnail uri",
      "post_views": 0,
      "post_likes": 0,
      "post_comment_count": 0,
      "post_description": "게시글 설명",
      "user_login_id": "login_id",
      "user_profile_image": "profile_image_uri",
      "post_id": 234,
      "user_id": 3,
      "create_at": "2022-12-08T04:35:11.000Z"
    }
  ]
}
```

- series : 설정된 시리즈의 정보 및 게시글 목록
- post : 게시글의 상세 페이지 내용.
  - is_writer : 로그인한 사용자와 작성자가 일치 1 / 불일치 0
  - is_follower : 로그인한 사용자와 작성자가 팔로우 상태면 1 / 팔로우가 아닐 경우 0
  - is_liked : 로그인한 사용자가 해당 게시글을 좋아요 했을 경우 1 / 아닐 경우 0
- next_post : 다음 게시글 정보
- pre_post : 이전 게시글 정보
- comments : 게시글에 작성된 댓글들의 목록.
  - is_comments_writer : 로그인한 사용자와 작성자가 일치 1 / 불일치 0
- interested : 관심 있을 만한 포스트들의 목록.

</details>
