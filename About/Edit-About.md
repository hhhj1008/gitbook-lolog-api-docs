# 소개글 편집

## CreatePost - 소개글 편집

![](https://img.shields.io/badge/PATCH-yellow?style=plastic\&logo=appveyor\&logo=PATCH) http://localhost:8000/about

### Parameter

**authorization - Bearer Token**

* login 시 발급 받은 access token

**body - json**

```json
{
  "about_blog": "편집할 소개글 내용"
}
```

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

\


![](https://img.shields.io/badge/400-DB3A00?style=plastic\&logo=appveyor\&logo=400) BadRequestException

<details>

<summary>오류 내용</summary>

```json
{
  "statusCode": 400,
  "message": "...."
}
```

* 데이터를 보내는 과정에서 잘못된 데이터가 왔을 경우 발생하는 오류\
  ex) 잘못된 파라메터명, 혹은 알맞지 않은 데이터 및 타입

</details>
