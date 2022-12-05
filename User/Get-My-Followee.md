# 내가 팔로우한 목록

## GetMyFollowee - 내가 팔로우한 목록

<img src="https://img.shields.io/badge/GET-green?style=plastic&logo=appveyor&logo=GET"/> http://localhost:8000/users/follow

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/>

<details>
<summary>결과 값</summary>
<div markdown="1">

```json
{
    "follow": [
        {
            "name": "안수철1",
            "title": "josephscahn1.log",
            "about_me": "josephscahn1",
            "followee_id": 1,
            "profile_image": null
        },
        ...
    ]
}

// 팔로우한 목록이 없을 때
{}
```

</div>
</details>
