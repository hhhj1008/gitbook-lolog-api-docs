# 소개글 조회

## SelectAbout - 소개글 조회

![](https://img.shields.io/badge/GET-blue?style=plastic\&logo=appveyor\&logo=GET) http://localhost:8000/about/{user\_id}

### Parameter

**parma**

* user\_id : 조회할 소개글의 작성자 ID

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic\&logo=appveyor\&logo=200) 성공

<details>

<summary>결과 값</summary>

```json
{
  "statusCode": 200,
  "about": {
    "user_id": 3,
    "about_blog": "소개글 내용",
    "is_owner": 1
  }
}
```

* user\_id: 소개글을 작성한 사용자의 ID
* about\_blog: 소개글 내용
* is\_owner: 소개글을 작성자와 로그인한 사용자가 일치할 경우 1, 일치하지 않을 경우 0

</details>
