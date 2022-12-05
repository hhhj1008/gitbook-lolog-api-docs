# 팔로우

## Follow - 팔로우

<img src="https://img.shields.io/badge/POST-green?style=plastic&logo=appveyor&logo=POST"/> http://localhost:8000/users/follow

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "followee_id": 1
}
```

followee_id: 내가 팔로우하려는 유저의 아이디

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "follow success"
}
```

</div>
</details>

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
  "message": "Already follow"
}
```

</div>
</details>
