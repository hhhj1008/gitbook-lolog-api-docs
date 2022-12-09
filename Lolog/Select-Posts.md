# 게시글 목록 & 태그 목록 조회

## SelectPosts&Tags - 게시글 목록 & 태그 목록 조회

<img src="https://img.shields.io/badge/GET-blue?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/lolog/{user_id}?offset=1&limit=5&tag_id={tag_id}

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
  "user": {
    "follow_count": "0",
    "id": 3,
    "profile_image": null,
    "name": "사용자 이름",
    "about_me": "사용자 한줄 소개",
    "title": "롤로그 제목",
    "email": "",
    "comment_alert": 0,
    "update_alert": 0,
    "social_info_email": "",
    "social_info_github": "",
    "social_info_twitter": "",
    "social_info_facebook": "",
    "social_info_url": ""
  },
  "posts": [
    {
      "post_title": "게시글 제목",
      "post_status": 1,
      "post_thumbnail": "",
      "post_likes": 0,
      "post_comment_count": 0,
      "post_description": "",
      "user_id": 3,
      "post_id": 257,
      "tags": [
        {
          "tag_id": 1,
          "tag_name": "태그"
        }
      ],
      "create_at": "2022-12-09T02:56:15.614Z"
    }
  ],
  "tags": [
    {
      "post_count": "0",
      "tag_id": "0",
      "name": "전체보기"
    },
    {
      "post_count": "1",
      "tag_id": "1",
      "name": "태그"
    }
  ]
}
```

- user: 롤로그 소유자의 정보
- posts : 게시글 들의 목록. 로그인한 사용자와 롤로그 소유자의 ID가 일치할 경우 비공개로 작성한 목록도 보여줌. (post_status: 1(공개)/2(비공개))
- tags : 롤로그 소유자가 사용한 태그들의 목록

</div>
</details>

<br>

<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> BadRequestException

<details>

<summary>오류 내용</summary>

```json
{
  "statusCode": 400,
  "message": "...."
}
```

- 데이터를 보내는 과정에서 잘못된 데이터가 왔을 경우 발생하는 오류 <br> ex) offset 혹은 limit이 누락된 경우

</details>

![](https://img.shields.io/badge/422-DB3A00?style=plastic&logo=appveyor&logo=422) QueryFailedError

<details>

<summary>오류 내용</summary>

```json
{
  "statusCode": 422,
  "message": "...."
}
```

- 데이터를 조회 중 발생하는 데이터베이스 오류 <br> ex) 데이터베이스 쿼리 오타 혹은 잘못된 데이터를 전송할 경우.

</details>
