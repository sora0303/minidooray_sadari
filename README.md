# minidooray_sadari

# POST /api/accounts
### 계정 생성 요청
## Response
#### body
```
{
    "loginId": "",
    "password": "",
    "email": "",
    "name": ""
}
```

---
# GET /api/login?loginId={loginId}
### 로그인
## Response
#### body
```
{
    "loginId": "",
    "password": ""
}
```

---
# GET /api/auth/test
### 로그인후 요청

---
# GET /api/accounts/modify/{accountId}
### 수정할 계정 조회

---
# PUT /api/accounts/modify/{accountId}
### 계정 수정 요청
## Response
#### body
```
{
    "loginId": "",
    "password": "",
    "email": "",
    "name": "",
    "status": ""
}
```

---
# DELETE /api/accounts/{id}
### 계정 삭제 요청

---
# GET /api/accounts/group
### 모든 계정 조회

---

# POST /api/projects
### 프로젝트 등록
## Response
#### body
```
{
    "name": "프로젝트1",
    "description": "프로젝트 설명",
    "memberId": "1",
    "memberName": "홍길동"
}
```

---
# PUT /api/projects/{projectId}
### 프로젝트 수정 (기본설정)
## Response
#### body
```
{
  "status": "휴면",
  "name": "프로젝트 2 수정",
  "description": "프로젝트 설명 2 수정"
}
```

---
# DELETE /api/projects/{projectId}
### 프로젝트 삭제

---
# POST /api/projects/{projectId}/members
### 프로젝트 멤버 등록

```
{
  "memberId": 4,
  "memberName": "요요요"
}
```

---
# PUT /api/projects/{projectId}/members/{memberId}
### 프로젝트 멤버 역할 수정

```
{
  "role": "관리자"
}
```

---
# DELETE /api/projects/{projectId}/members/{memberId}
### 프로젝트 멤버 삭제

---
# GET /api/projects/members/{memberId}
### 멤버 아이다로 프로젝트 리스트 조회

---
# GET /api/projects/{projectId}
### 프로젝트 아이디로 프로젝트 조회

---
# GET /api/projects/{projectId}/members
### 프로젝트 아이디로 프로젝트 멤버 조회

---
# POST /api/projects/{projectId}/tasks
### 업무 등록
```
{
  "title": "미니두레이 ERD 설계2",
  "content": "ERD 설계 열심히 하기2",
  "writerId": 1,
  "endDate": "2023-06-01",
  "memberIds": [1, 2],
  "milestoneId": 1,
  "tagIds": [2, 3]
}
```

---
# PUT /api/projects/{projectId}/tasks/{taskId}
### 업무 수정

```
{
  "title": "미니두레이 ERD 설계 수정",
  "content": "ERD 설계 열심히 하기 수정",
  "endDate": "2023-06-10",
  "memberIds": [1, 2],
  "milestoneId": 2,
  "tagIds": [4]
}
```

---
# DELETE api/projects/{projectId}/tasks/{taskId}
### 업무 삭제

---
# GET /api/projects/{projectId}/tasks
### 프로젝트 아이디로 업무 조회

---
# GET /api/projects/{projectId}/tasks/{taskId}
### 업무 아이디로 업무 조회

---

# POST /api/tasks/{tasksId}/comments
### 댓글 등록

```
{
  "writerId": 1,
  "contents": "코멘트를 달아보았다3"
}
```

---
# PUT /api/tasks/{tasksId}/comments/{commentId}
### 댓글 수정

```
{
  "contents": "코멘트를 수정해보았다"
}
```

---
# DELETE /api/tasks/{tasksId}/comments/{commentId}
### 댓글 삭제

---
# POST /api/projects/{projectId}/milestones
### 마일스톤 등록

```
{
  "name": "마일스톤5",
  "startDate": "2023-04-28",
  "endDate": "2023-06-01"
}

```

---
# PUT /api/projects/{projectId}/milestones/{milestoneId}
### 마일스톤 수정

```
{
  "name": "마일스톤 수정",
  "startDate": "2023-04-29T00:00:00",
  "endDate": "2023-06-01"
}

```

---
# DELETE /api/projects/{projectId}/milestones/{milestoneId}
### 마일스톤 삭제


---
# GET /api/projects/{projectId}/milestones
### 프로젝트 아이디로 마일스톤 조회

---
# GET /api/projects/{projectId}/milestones/{milestoneId}
### 마일스톤 아이디로 마일스톤 조회
---

***
# POST /api/projects/{projectId}/tags
### 태그 등록

```
{
    "name": "태그1"
}
```

---
# PUT /api/projects/{projectId}/tags/{tagId}
### 태그 수정
```
{
    "name": "태그 수정"
}
```

---
# DELETE /api/projects/{projectId}/tags/{tagId}
### 태그 삭제

---


# GET /api/projects/{projectId}/tags
### 프로젝트 아이디로 태그 조회

---







