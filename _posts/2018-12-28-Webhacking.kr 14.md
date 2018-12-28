Webhacking.kr 14
================

<img width="228" alt="webhackin kr-14-1" src="https://user-images.githubusercontent.com/45537913/50507205-d0d28680-0abf-11e9-8379-28baa05c8755.png">

처음 문제에 들어가면 달랑 저거 하나만 있다. f12를 눌러 소스를 보았다.

<img width="365" alt="webhacking kr-14-2" src="https://user-images.githubusercontent.com/45537913/50507215-dc25b200-0abf-11e9-8eb7-673715831c4a.png">

function ck( )가 정의되어있다. ul이 pw.input_pwd.value일때 password is ~ 하면서 password가 나온다는 것을 알수 있다. ul이 정의 되있는것을 보면 url에서 .kr이 있는 인덱스를 저장하고 다시 이 인덱스를 30곱한 값이다.

.kr은 18번째에 있으나 index는 0부터 시작이므로 17 이 저장된다. 즉 마지막에 ul에 저장되는 값은 17*30 = 510 이므로 값을 아까 그 check에 넣으면 아래처럼 암호가 나온다.

<img width="446" alt="webhacking kr-14-4" src="https://user-images.githubusercontent.com/45537913/50507234-fb244400-0abf-11e9-8df0-03d4b6e12151.png">

위 암호를 auth에 가서 인증을 해주면<img width="696" alt="webhacking kr-14-6" src="https://user-images.githubusercontent.com/45537913/50507259-18f1a900-0ac0-11e9-84ac-53ffda7d63ea.png">

<img width="450" alt="webhacking kr-14-5" src="https://user-images.githubusercontent.com/45537913/50507254-0f684100-0ac0-11e9-94ab-02ac6c44ecbb.png">

chalenge 14 clear!!
