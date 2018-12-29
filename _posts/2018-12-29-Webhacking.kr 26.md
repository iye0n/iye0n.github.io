Webhacking.kr 26
================

<img width="450" height="400" alt="webhacking kr-26-1" src="https://user-images.githubusercontent.com/45537913/50535865-a81ac180-0b91-11e9-808b-a47cc55c802f.png">

일단 소스를 보았다. 소스에는 eregi 함수와 ulrdecode 함수가 있는 코드가 있었다. 내 목표는 solve 함수를 실행시키는 것 이므로 GET[id] == "admin"을 만족시키면 되는 문제였다.

코드를 보면 GET[id]의 값을 받고 이것을 urldecode한 값을 admin과 비교하는것 이므로 admin을 urlencode 를 해서 넣어봤다. 주소의 마지막에 ?id=%61%64%6d%69%6e 라고 넣게되었다.

<img width="450" height="100" alt="webhacking kr-26-2" src="https://user-images.githubusercontent.com/45537913/50535867-afda6600-0b91-11e9-979b-61a277d15c81.png">

넣었더니 no!라고 뜨면서 주소의 마지막이 id=admin으로 되어있었다. 아마 값을 넘기면서 자동적으로 urldecode가 한번 된 뒤, eregi에 걸린것 같다는 생각을 했다. 그래서 urlencode가 두번 된 값을 id=%2561%2564%256d%2569%256e라고 넣어보았다.

<img width="450" height="100" alt="webhacking kr-26-3" src="https://user-images.githubusercontent.com/45537913/50535868-b23cc000-0b91-11e9-94f3-f0c10256672b.png">

Congratulation! 이 떴다.

웹 서버와 브라우져 사이에서 데이터 교환시 브라우저는 폼에서 입력받은 데이터를 자동으로 인코딩 한 값을 php로 보내고 php는 받은 인코딩 된 값을 자동으로 디코딩 하기 때문에 두번 인코딩한 값을 넣어주는게 맞았던 것이었다.

<img width="450" height="200" alt="webhacking kr-26-4" src="https://user-images.githubusercontent.com/45537913/50535869-b49f1a00-0b91-11e9-954a-34d802d66a34.png">

26 clear!
