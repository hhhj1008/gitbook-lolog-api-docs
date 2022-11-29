# 댓글 삭제

## DeleteCommnet - 댓글 삭제

<img src="https://img.shields.io/badge/DELETE-red?style=plastic&logo=appveyor&logo=DELETE"/> http://localhost:8000/comments/{post_id}/{comment_id}

### Parameter

**authorization - Bearer Token**

- login 시 발급 받은 access token

**parma**

- post_id : 댓글이 포함된 게시글의 ID
- comment_id : 수정할 댓글의 ID

### Responses

<img src="https://img.shields.io/badge/200-519800?style=plastic&logo=appveyor&logo=200"/> comment delete success

<img src="https://img.shields.io/badge/403-DB3A00?style=plastic&logo=appveyor&logo=403"/> comment delete failed
