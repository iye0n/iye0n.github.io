---
layout: post
title: "Webhacking.kr 38"
subtitle: ""
date: 2018-12-29 18:33:29
background: '/img/bg-post.jpg'
---
Webhacking.kr 38
================

<img width="260" alt="webhacking kr-38-1" src="https://user-images.githubusercontent.com/45537913/50536692-5e82a480-0b9a-11e9-89b9-fbafdffdad6e.png">

Log injection 문제이다. Log injection 에 대해서는 따로 정리해두었다. 일단 admin을 넣어보았다. 정답이 아니였다. 그래서 guest 를 쓰고 login을 한 다음 admin 버튼을 눌러보았다.

<img width="260" alt="webhacking kr-38-2" src="https://user-images.githubusercontent.com/45537913/50536693-5fb3d180-0b9a-11e9-8339-ecc2fed8407b.png">

admin을 누르면 log 가 뜨는데 저장되는 형식이 ip : 넣은 값 이었다.

그렇다면 내가 나타내야할 값은 ip : admin 이므로 로그인 할때 값을

**guest ip:admin** 으로 넣었다.

<img width="400" alt="webhackin kr-38-3" src="https://user-images.githubusercontent.com/45537913/50536696-62162b80-0b9a-11e9-92c0-fa7f7ca6986f.png">

Congratulation! 이 떴다. 매우 간단한 log injection 문제였다.

<img width="400" alt="webhacking kr-38-4" src="https://user-images.githubusercontent.com/45537913/50536698-64788580-0b9a-11e9-9864-db4a1eacf1fc.png">

38 clear!
