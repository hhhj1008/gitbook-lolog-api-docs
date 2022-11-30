# 알림 수정

## UpdateUser - 알림 수정

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/users/type=alert

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "comment_alert": 0,
  "update_alert": 1
}
```

### 현재 예외처리의 부족으로 comment_alert랑 update_alert 값이 안들어오면 서버가 터집니다

### 꼭 둘 다 입력해주세요,,

### 조만간 예외처리 하겠습니다,,

### Responses

<img src="https://img.shields.io/badge/201-519800?style=plastic&logo=appveyor&logo=201"/> update user success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
  "message": "update user success",
  "data": {
    "comment_alert": 1,
    "update_alert": 0
  }
}
```

</div>
</details>
<br>
<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> title must be entered

<details>
<summary>결과 값 - 0,1 이외의 값이 들어온 경우</summary>
<div markdown="1">

```json
{
  "statusCode": 400,
  "message": ["comment_alert must be a 1 or 0 or Null"],
  "error": "Bad Request"
}
```

</div>
</details>
<br>
<img src="https://img.shields.io/badge/400-DB3A00?style=plastic&logo=appveyor&logo=400"/> title must be entered

<details>
<summary>(업데이트 후 예정)결과 값</summary>
<div markdown="1">

```json
{
  "statusCode": 400,
  "message": "comment_alert must be entered",
  "error": "Bad Request"
}
```

</div>
</details>
