Webhacking.kr-6
===============

<img width="400" alt="webhacking kr -6-1" src="https://user-images.githubusercontent.com/45537913/50506440-56543780-0abc-11e9-9da1-a725abe5d24c.png">

6번 문제를 보면 힌트가 쓰여져 있고 hint가 base64이고 index.phps로 되어있다. index.phps를 누르면 아래와 같은 코드가 쓰여져 있다.

<img width="400" alt="webhacking kr -6-2" src="https://user-images.githubusercontent.com/45537913/50506456-6b30cb00-0abc-11e9-85ac-7a8c3829b11e.png"><img width="600" alt="webhacking kr -6-3" src="https://user-images.githubusercontent.com/45537913/50506464-74ba3300-0abc-11e9-8d30-9bb7650d2a37.png">

코드를 잘 살펴보면 decode_id == "admin" 이고, decode_pw == "admin"이면 slove 함수가 실행된다는 것을 알 수있다. decode_id 는 base64_decode 함수에 decode_id를 넣은 값이고, decode_pw 는 base64_decode에 decode_pw를 넣은것이므로 password 에 해당하는 쿠키에 admin을 base64로 암호화한 값을 넣으면 되고, 마찬가지로 user에 해당하는 쿠키에 admin을 base64로 암호화한 값을 넣으면 된다.

<img width="500" alt="webhacking kr -6-4" src="https://user-images.githubusercontent.com/45537913/50506469-7d126e00-0abc-11e9-9058-d15715173ab4.png">

이런식으로 각각 해당하는 쿠키에 넣으면

<img width="400" alt="webhacking kr -6-5" src="https://user-images.githubusercontent.com/45537913/50506480-87cd0300-0abc-11e9-97c9-42976b292127.png">

solve 함수가 실행되면서 congratualtion!이 뜬다.
