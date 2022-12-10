# 시리즈 수정

## createSeries - 시리즈 수정

![](https://img.shields.io/badge/PATCH-yellow?style=plastic\&logo=appveyor\&logo=PATCH) http://localhost:8000/series/{series\_id}

### Parameter

**authorization - Bearer Token**

* login 시 발급 받은 access token

**query**

* series\_id : 수정하려는 시리즈의 ID

**body - json**

```json
{
  "series_name": "수정할 시리즈 이름"
  "sort": [
    { "post_id": "1", "sort": 1 },
    { "post_id": "2", "sort": 2 }
  ]
}
```

* series\_name : 수정할 시리즈 이름
* sort : post\_id 와 정렬 순서(sort)를 배열로 작성

### Responses

![](https://img.shields.io/badge/200-519800?style=plastic\&logo=appveyor\&logo=200) update seires success

<details>

<summary>결과 값</summary>

```json
```

</details>

\


![](https://img.shields.io/badge/403-DB3A00?style=plastic\&logo=appveyor\&logo=403) update seires failed
