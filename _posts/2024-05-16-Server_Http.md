---
title: Web Server based on http module
date: 2024-05-16 12:30:00 +09:00
categories: [Studying, Node.js]
tags: 
  [make, server, http]
---

```jsx
const http = require('http'); // http 라이브러리를 require 함수를 통해 포함시킴.

const hostname = '127.0.0.1';
const port = 8080;

// createServer()는 http 모듈로 서버를 생성함.
const server = http.createServer((req,res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

// listen()은 대기하는 함수로, 서버의 등록한 아이피와 포트 번호를 기반으로 클라이언트가 서버에 접속하기 전까지 대기함.
server.listen(port, hostname, () => {
  console.log(`server running at http://${hostname}:${port}/`);
})
```

