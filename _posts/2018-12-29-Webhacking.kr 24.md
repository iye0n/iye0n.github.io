---
layout: post
title: "Webhacking.kr 24"
subtitle: ""
date: 2018-12-25 18:33:29
background: '/img/bg-post.jpg'
---
Webhacking.kr 24
================

처음 문제에 들어갔을 때 Wrong ip! 라고 뜨는 화면이 나왔다. 그래서 일단 소스를 보았다.

<img width="402" alt="webhacking kr-24-3" src="https://user-images.githubusercontent.com/45537913/50535829-5a9e5480-0b91-11e9-950e-9a5d244d0d79.png">

ip에서 '12', '7.', '0.'를 빈칸으로 바꾸는 코드 ip가 127.0.0.1 이면 solve 함수를 실행시켜주는 코드가 있었다.

그렇다면 빈칸으로 바꾸는 코드를 거쳤을 때, 127.0.0.1 이 되야하므로 ip를 1122.77..00..00..1로 바꾸면 된다.

<img width="320" alt="webhacking kr-24-4" src="https://user-images.githubusercontent.com/45537913/50535831-5a9e5480-0b91-11e9-9960-0c5f4929bb05.png">

cookie 에 REMOTE_ADDR를 만든 뒤 값을 위처럼 넣어주면

<img width="443" alt="webhacking kr-24-5" src="https://user-images.githubusercontent.com/45537913/50535832-5a9e5480-0b91-11e9-8f50-0773439cba0d.png">

Congratulation! 문제 clear

<img width="144" alt="webhacking kr-24-6" src="https://user-images.githubusercontent.com/45537913/50535833-5b36eb00-0b91-11e9-83c3-6e1b51d78614.png">

값을 넣은 페이지는 아래와 같다.
