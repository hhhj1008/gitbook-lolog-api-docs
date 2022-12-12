# 메인페이지 게시글 조회

## 메인페이지 조회

![](https://img.shields.io/badge/GET-blue?style=plastic\&logo=appveyor\&logo=GET) http://localhost:8000/main?type=trand\&period=\&offset=1\&limit=10

{% hint style="info" %}
* 최신으로 조회 시, 최근 작성된 게시글 순으로 정렬되어 데이터가 보여짐.
* 트렌딩으로 조회 시, 조회 수와 좋아요 수를 합산하여 가장 높은 것부터 데이터가 보여짐.\
  조회 수와 좋아요 수가 0일 경우엔 목록에서 제외 됨.
{% endhint %}

**query**

* type : trend(트렌딩) / recent(최신)
* period : today(오늘) / week(이번 주) / month(이번 달) / year(올해)\
  트랜딩으로 조회 시에 기간 입력 필수
* offset : 페이지의 번호 (필수)
* limit : 한 페이지에서 보여지는 게시글의 갯수 (필수)

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic\&logo=appveyor\&logo=200) 성공

<details>

<summary>결과 값</summary>

```json
{
  "statusCode": 200,
  "post": [
    {
      "post_title": "게시글 제목",
      "post_thumbnail": "thumbnail uri",
      "post_views": 3,
      "post_likes": 1,
      "post_comment_count": 0,
      "post_description": "게시글 소개",
      "user_login_id": "user_login_id",
      "user_profile_image": null,
      "user_id": 8,
      "post_id": 270,
      "create_at": "2022-12-11T19:18:33.864Z"
    }
  ]
}
```

* post\_title: 게시글의 제목
* post\_thumbnail: 게시글의 썸네일
* post\_views : 게시글의 조회 수
* post\_likes : 게시글의 좋아요 수
* post\_comment\_count : 게시글의 댓글 수
* post\_description : 게시글에 대한 소개
* user\_login\_id : 작성한 사용자의 login ID
* user\_profile\_image: 작성한 사용자의 프로필 이미지
* user\_id : 작성한 사용자의 ID
* post\_id : 게시글의 ID
* create\_at : 게시글의 작성 일자.

</details>
