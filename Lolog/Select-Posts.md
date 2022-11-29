# 게시글 목록 & 태그 목록 조회

## SelectPosts&Tags - 게시글 목록 & 태그 목록 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/lolog/{user_id}?offset=3&limit=5&tag_id=1

### Parameter

**parma**

- user_id : 롤로그 소유자의 ID

**query**

- offset : 페이지의 번호 (필수)
- limit : 한 페이지에서 보여지는 게시글의 갯수 (필수)
- tag_id : 선택한 태그에 포함된 게시글 목록을 조회할 때 사용 (선택)

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> 게시글 목록 & 태그 목록 조회 성공

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 200,
  "posts": [
    {
      "post_title": "제목",
      "post_content": "내용",
      "post_status": 1,
      "post_thumbnail": "",
      "post_likes": 0,
      "post_comment_count": 0,
      "post_create_at": "2022-11-18T13:54:37.144Z",
      "user_id": 1,
      "post_id": 5,
      "tags": null
    },
    {
      "post_title": "제목",
      "post_content": "내용",
      "post_status": 2,
      "post_thumbnail": "",
      "post_likes": 0,
      "post_comment_count": 0,
      "post_create_at": "2022-11-18T12:53:53.613Z",
      "user_id": 1,
      "post_id": 2,
      "tags": null
    },
    {
      "post_title": "제목",
      "post_content": "내용",
      "post_status": 2,
      "post_thumbnail": "",
      "post_likes": 0,
      "post_comment_count": 0,
      "post_create_at": "2022-11-18T12:03:16.486Z",
      "user_id": 1,
      "post_id": 1,
      "tags": null
    }
  ],
  "tags": [
    {
      "post_count": "5",
      "tag_id": 1,
      "name": "태그1"
    },
    {
      "post_count": "3",
      "tag_id": 2,
      "name": "태그2"
    },
    {
      "post_count": "1",
      "tag_id": 3,
      "name": "태그3"
    }
  ]
}
```

- posts : 게시글 들의 목록. 로그인한 사용자와 롤로그 소유자의 ID가 일치할 경우 비공개로 작성한 목록도 보여줌. (post_status: 1(공개)/2(비공개))
- tags : 롤로그 소유자가 사용한 태그들의 목록

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> 게시글 목록 & 태그 목록 조회 실패
