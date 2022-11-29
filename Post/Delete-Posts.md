# 게시글 삭제

## DeletePost - 게시글 삭제

<img src="https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE"/> http://localhost:8000/posts/{post_id}?status=1

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**param**

- post_id : 삭제하고자 하는 게시글의 ID

**query**

- status : 게시글의 상태 값. 1(공개) / 2(비공개) / 3(임시글)

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> post delete success

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> post delete failed
