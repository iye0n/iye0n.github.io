Webhacking.kr - join
====================

사이트에 처음 들어가게 되면, 아래와 같이 로그인 화면만 있고 계정 가입 화면은 없다. ![webhacking_kr-login1](https://user-images.githubusercontent.com/45537913/50384252-d3bb2900-0705-11e9-8a6e-6d18ce6d683a.jpg) 그렇다면 가입 버튼을 띄워야한다는 소리일것이므로 크롬 브라우져에서 F12를 눌러 소스를 보았다.

![webhacking.kr-login2](https://user-images.githubusercontent.com/45537913/50384261-e3d30880-0705-11e9-80a1-11e9ba84e76b.png) 소스를 확인했더니 주석처리로 register부분이 있었다. 주석을 없애고 <input type= 부터
 ~/tr> 만 남겨두고 다 삭제를 했다.

![webhacking.kr-login3](https://user-images.githubusercontent.com/45537913/50384269-f64d4200-0705-11e9-9c28-83bcec212514.png) 위 사진이 그 결과이다. register 버튼이 나타났으니 눌러서 안에 들어가보면 회원가입 창이 나타난다. ![webhacking.kr-login4](https://user-images.githubusercontent.com/45537913/50384276-049b5e00-0706-11e9-803f-2858b5f6a636.png) 내가 쓸 아이디와 패스워드, 이메일을 입력하고 decode me에 해당하는 영어 문자열을 decode 해서 넣어주면 회원가입이 완료된다. 해당 문자열을 base 64 로 디코딩 하면 숫자 열이 나오는데 그것이 답이다.

이렇게 해서 회원가입은 끝이난다!
