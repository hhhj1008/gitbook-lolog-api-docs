# 시리즈 수정

## createSeries - 시리즈 수정

<img src="https://img.shields.io/badge/PATCH-yellow?style=plastic&logo=appveyor&logo=PATCH"/> http://localhost:8000/lolog/{user_id}/series/{series_id}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**body - json**

```json
{
  "sort": [
    { "post_id": "1", "sort": 1 },
    { "post_id": "2", "sort": 2 },
    ...
  ]
}
```

- sort : post_id 와 정렬 순서(sort)를 배열로 작성

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> update seires success

<details>
<summary>결과 값</summary>
<div markdown="1">

```json

```

<!-- 수정 후 정렬된 순서대로 결과 값 반환하도록 수정 필요 -->

</div>
</details>

<br>

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> update seires failed
