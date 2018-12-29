---
layout: post
title: "Log injection"
subtitle: ""
date: 2018-12-29 18:33:29
background: '/img/bg-post.jpg'
---

Log injection
=============

log injection 이란 spl injection 처럼 파라미터를 통해 로깅을 조절하는 방법이다.

일반적으로 로그인에 대한 로깅을 조절한다.

```
String userid = request.getParameter("userid");

if (로그인성공)

    log.write("Login succeeded for : " + userid);

else

    log.write("Login failed for : " + userid);
```

를 하면

Login succeeded for : **guest**

Login succeeded for : **admin**

이렇게 프린트 된다. 그렇다면 로그인시

guest \n Login succeeded for : admin 을 하면

로그 결과는 다음과 같이 출력 될 것이다.

Login succeeded for : **guest**

**Login succeeded for : admin**

Login succeeded for : **admin**

이처럼 log injection 공격을 할 수 있다.
