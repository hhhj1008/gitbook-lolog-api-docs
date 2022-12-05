# 언팔로우

## Follow - 언팔로우

<img src="https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE"/> http://localhost:8000/users/follow

### Parameter

**body - json**

```json
{
  "followee_id": 1
}
```

followee_id: 내가 언팔로우하려는 유저의 아이디

### Responses

<img src="https://img.shields.io/badge/204-519800?style=plastic&logo=appveyor&logo=204"/>

<br>

<img src="https://img.shields.io/badge/404-DB3A00?style=plastic&logo=appveyor&logo=404"/> 
<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 404,
  "message": "Not Found UserId"
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> 
<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 400,
  "message": "Cannot follow yourself"
}
```

</div>
</details>

<br>

<img src="https://img.shields.io/badge/409-DB3A00?style=plastic&logo=appveyor&logo=409"/> 
<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 409,
  "message": "Already unfollow"
}
```

</div>
</details>
