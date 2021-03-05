---
title: 외근기록보드 API

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript

toc_footers:
  - ecplaza

includes:
  - errors

search: true

code_clipboard: true
---

# Overview

##외근기록보드
- 외근 기록 목록을 가져올 수 있는 API 입니다.

항목명 | 값 
---------- | ----------
개발언어 | JAVA
데이터베이스 | MariaDB
운영체제 | Window10
도구 | IntelliJ


# Request
###요청주소
GET 
###요청메소드
http://<code>domain</code>/api/v1/outworks

<aside class="notice">
 <code>domain</code> 자리에 주소가 채워져야 합니다.
</aside>

# Respond
## 외근목록 얻어오기

> 아래와 같은 JSON 구조를 return 합니다:

```json
{
  "status": 1,
  "data":[
        {
          "name": "임다은", 
          "phone": "01000000000", 
          "destination": "본사",
          "type":"외근",
          "latitude" : "37.5277834127565", 
          "longitude": "127.12157116767759",
          "description": "외근보드견학", 
          "start_time": "2021-02-15 10:10:05",  
          "finish_time": "2021-02-15 11:10:45",
        } 
  ],
  "message": "success",
}

```

외근 기록의 목록을 얻어옵니다.

<aside class="success">
IP로 접근을 제어해 허용된 사용자만이 접근 가능합니다.
</aside>

### 출력결과

항목명 | 값 | 설명 
---------- | ---------- | ----------
status | Integer | 상태
data | 배열 | 외근 정보 배열 
message | String | 오류 메시지

### data

항목명 | 값 | 설명 | 기타
---------- | ---------- | ---------- | ----------
name | String | 사원명 |
phone | String | 전화번호 |
destination | String | 행선지 |
latitude | String | 현 위치(위도) |
longitude | String | 현 위치(경도) |
type | String | 외근유형 |
description | String | 용무 |
start_time | String | 시작시각 | yyyy-MM-dd HH:mm:ss
finish_time | String | 종료시각 | yyyy-MM-dd HH:mm:ss
