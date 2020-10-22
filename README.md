# **Design FIR filter**

[Untitled](https://www.notion.so/69b1ac9fc9694814aea32568db965a18)

설계의 구성요소와 현실적 제한조건 고려여부

Ⅰ. Problem Formulation

Input Signal
![https://blog.kakaocdn.net/dn/bHhkRB/btqLxvA3e3Z/crzT7ZpRkNA8RdkbESxEYk/img.jpg](https://blog.kakaocdn.net/dn/bHhkRB/btqLxvA3e3Z/crzT7ZpRkNA8RdkbESxEYk/img.jpg)
Output Signal
![https://blog.kakaocdn.net/dn/uCWgT/btqLzF4cQrz/LjLsfr3uC1iPo4oFUwCWh1/img.jpg](https://blog.kakaocdn.net/dn/uCWgT/btqLzF4cQrz/LjLsfr3uC1iPo4oFUwCWh1/img.jpg)
![https://blog.kakaocdn.net/dn/bBRuZd/btqLwLRFQeT/ukNOIlwhfvzkoKKqR65NEk/img.jpg](https://blog.kakaocdn.net/dn/bBRuZd/btqLwLRFQeT/ukNOIlwhfvzkoKKqR65NEk/img.jpg)
: arbitrary amplitude,
![https://blog.kakaocdn.net/dn/ts144/btqLvfsooI7/1TWo7oqoQSEER6RxEcw9E1/img.jpg](https://blog.kakaocdn.net/dn/ts144/btqLvfsooI7/1TWo7oqoQSEER6RxEcw9E1/img.jpg)
: arbitrary phase
FIR Filter length : 12
Ⅱ. Report
입력신호에서 가장 큰 주파수 f = 300Hz 이며 Nyquist 정리에 의하면 입력 신호의 최대 주파수보다 최소한 2배는 빠르게 샘플링해야 본래 신호를 충분히 재현할 수 있기 때문에 샘플링주파수를 600Hz 으로 잡았다.
따라서
![https://blog.kakaocdn.net/dn/bwRwUE/btqLyKLqYoN/wJhLxgEtmujfghRiS3g7J0/img.jpg](https://blog.kakaocdn.net/dn/bwRwUE/btqLyKLqYoN/wJhLxgEtmujfghRiS3g7J0/img.jpg)
가 되며
![https://blog.kakaocdn.net/dn/TFTSy/btqLxuoy5Va/Sld1jRpRNuerS2ymOjGDu0/img.jpg](https://blog.kakaocdn.net/dn/TFTSy/btqLxuoy5Va/Sld1jRpRNuerS2ymOjGDu0/img.jpg)
가 된다.
![https://blog.kakaocdn.net/dn/bbPHg2/btqLzXctXGn/CAfBfEumInm1E1yXL0PkC1/img.jpg](https://blog.kakaocdn.net/dn/bbPHg2/btqLzXctXGn/CAfBfEumInm1E1yXL0PkC1/img.jpg)
은 주파수가
![https://blog.kakaocdn.net/dn/cfCDFk/btqLA4Ca23e/xWQc2KtYanTTel4hf0ppp0/img.jpg](https://blog.kakaocdn.net/dn/cfCDFk/btqLA4Ca23e/xWQc2KtYanTTel4hf0ppp0/img.jpg)
일 때의 값만 나타나므로 FIR 필터에서 유일하게
![https://blog.kakaocdn.net/dn/bIrs1T/btqLvfsooJd/tmTdgZAn6uCf1Z3qP2gHoK/img.jpg](https://blog.kakaocdn.net/dn/bIrs1T/btqLvfsooJd/tmTdgZAn6uCf1Z3qP2gHoK/img.jpg)
인 지점에만 영점이 없음을 예상할 수 있다.
FIR Filter 의 길이가 12 로 주어졌으므로
![https://blog.kakaocdn.net/dn/YHo3N/btqLxvVhl91/f1gTwuwz2NQK3bIzKkiqe1/img.jpg](https://blog.kakaocdn.net/dn/YHo3N/btqLxvVhl91/f1gTwuwz2NQK3bIzKkiqe1/img.jpg)
이다.
![https://blog.kakaocdn.net/dn/2z7sM/btqLzXQ34fK/jQkVoOT94lggAQ6KBKY0s1/img.jpg](https://blog.kakaocdn.net/dn/2z7sM/btqLzXQ34fK/jQkVoOT94lggAQ6KBKY0s1/img.jpg)
이며 위 아래에
![https://blog.kakaocdn.net/dn/mICBx/btqLvFqOxOE/KLg8SH2OoAf9RhnuLOpbN1/img.jpg](https://blog.kakaocdn.net/dn/mICBx/btqLvFqOxOE/KLg8SH2OoAf9RhnuLOpbN1/img.jpg)
를 곱해주면
![https://blog.kakaocdn.net/dn/ba7KXw/btqLxv8NVpf/oFbmNKCWqascIo5nSrEGmK/img.jpg](https://blog.kakaocdn.net/dn/ba7KXw/btqLxv8NVpf/oFbmNKCWqascIo5nSrEGmK/img.jpg)
이 된다.
![https://blog.kakaocdn.net/dn/bZQ2Gd/btqLwLRFQeZ/qveWunKy2E1sZLQRMfoKh0/img.jpg](https://blog.kakaocdn.net/dn/bZQ2Gd/btqLwLRFQeZ/qveWunKy2E1sZLQRMfoKh0/img.jpg)
을 해로 가지므로
![https://blog.kakaocdn.net/dn/TqpUs/btqLzF4cQrM/KVvyaCc3NXgTeiVUPLIQoK/img.jpg](https://blog.kakaocdn.net/dn/TqpUs/btqLzF4cQrM/KVvyaCc3NXgTeiVUPLIQoK/img.jpg)
이다.

따라서

![https://blog.kakaocdn.net/dn/PsVzH/btqLxu9UUqJ/ol6BAFiKIuA7keBCaEiZ81/img.jpg](https://blog.kakaocdn.net/dn/PsVzH/btqLxu9UUqJ/ol6BAFiKIuA7keBCaEiZ81/img.jpg)

가 된다.

![https://blog.kakaocdn.net/dn/clsvzd/btqLwezJ1tR/iwVFKqYPhZGIcVobZRP9ek/img.jpg](https://blog.kakaocdn.net/dn/clsvzd/btqLwezJ1tR/iwVFKqYPhZGIcVobZRP9ek/img.jpg)

이

![https://blog.kakaocdn.net/dn/LFFAl/btqLzYWK7E4/7fvin6SG05FKpEZom8zKn1/img.jpg](https://blog.kakaocdn.net/dn/LFFAl/btqLzYWK7E4/7fvin6SG05FKpEZom8zKn1/img.jpg)

는 다음과 같은 pole-zero plot을 나타낸다.

이 그래프를

![https://blog.kakaocdn.net/dn/A7mf3/btqLA3Xzu3R/hConxGFYkSCHurG01nxAYk/img.jpg](https://blog.kakaocdn.net/dn/A7mf3/btqLA3Xzu3R/hConxGFYkSCHurG01nxAYk/img.jpg)

이 되도록 영점의 위치를 옮겨주거나 회전을 시켜줘야 한다.

pole-zero plot에서 반드시 복소수는 공액관계를 가져야 하므로 method 2를 사용하여 회전을 하는 방법이 편리하다.

![https://blog.kakaocdn.net/dn/7kEnn/btqLzYoUD9r/UdoWttFPaKkHe4DkUNWZZK/img.jpg](https://blog.kakaocdn.net/dn/7kEnn/btqLzYoUD9r/UdoWttFPaKkHe4DkUNWZZK/img.jpg)

이므로

![https://blog.kakaocdn.net/dn/daMFpW/btqLA2K8csh/jvIPT1soGk73LYxnJFqxd0/img.jpg](https://blog.kakaocdn.net/dn/daMFpW/btqLA2K8csh/jvIPT1soGk73LYxnJFqxd0/img.jpg)

가 4 일 때 영점이 없도록 회전을 해줘야 한다.

공액복소관계를 만들기 위해 전달함수를 2개로 각각 회전시킨다.

![https://blog.kakaocdn.net/dn/2qOBq/btqLveUu74U/Q5aVf8o9YjK9OQZPZTrzw0/img.jpg](https://blog.kakaocdn.net/dn/2qOBq/btqLveUu74U/Q5aVf8o9YjK9OQZPZTrzw0/img.jpg)

![https://blog.kakaocdn.net/dn/csHKtT/btqLxvnuM1j/k7VDYjUpouQnDAUlIOBqu0/img.jpg](https://blog.kakaocdn.net/dn/csHKtT/btqLxvnuM1j/k7VDYjUpouQnDAUlIOBqu0/img.jpg)

두 식을 더해주면

![https://blog.kakaocdn.net/dn/b4omT9/btqLzXjgpO5/wsrFvS2HUm8aZkPFV5atd0/img.jpg](https://blog.kakaocdn.net/dn/b4omT9/btqLzXjgpO5/wsrFvS2HUm8aZkPFV5atd0/img.jpg)

가 된다.

![https://blog.kakaocdn.net/dn/cajs23/btqLzYvHEy7/rWSOe4fsWNHbfDfvU6ycH0/img.jpg](https://blog.kakaocdn.net/dn/cajs23/btqLzYvHEy7/rWSOe4fsWNHbfDfvU6ycH0/img.jpg)

이므로 양변을 2로 나눠주면

![https://blog.kakaocdn.net/dn/bDRjTF/btqLzFwjGHd/9u15V1g0XpZlyKVrMNzGR1/img.jpg](https://blog.kakaocdn.net/dn/bDRjTF/btqLzFwjGHd/9u15V1g0XpZlyKVrMNzGR1/img.jpg)

가 된다.

![https://blog.kakaocdn.net/dn/bv4SbU/btqLveGXLTr/ujdk9JIARioQClnVVVgBs1/img.jpg](https://blog.kakaocdn.net/dn/bv4SbU/btqLveGXLTr/ujdk9JIARioQClnVVVgBs1/img.jpg)

그러면 최종적으로

![https://blog.kakaocdn.net/dn/YB7SX/btqLyKLqYu1/12QsRfZF2nrYZlYLiOMZVk/img.jpg](https://blog.kakaocdn.net/dn/YB7SX/btqLyKLqYu1/12QsRfZF2nrYZlYLiOMZVk/img.jpg)

의 pole-zero plot을 그리면 다음과 같다.

Z 대신에

![https://blog.kakaocdn.net/dn/lNkPE/btqLvGDfHrw/3d2KU9Rf8NWk8DlbX65xK0/img.jpg](https://blog.kakaocdn.net/dn/lNkPE/btqLvGDfHrw/3d2KU9Rf8NWk8DlbX65xK0/img.jpg)

를 대입하면 주파수 응답을 얻을 수 있으며 전달함수의 주파수 응답은 다음과 같다.

![https://blog.kakaocdn.net/dn/6J47Y/btqLxvHMmyE/l6cLqZ1X2Lo3i0RSyFP36k/img.jpg](https://blog.kakaocdn.net/dn/6J47Y/btqLxvHMmyE/l6cLqZ1X2Lo3i0RSyFP36k/img.jpg)

필터의 임펄스 응답은

![https://blog.kakaocdn.net/dn/dIHQaC/btqLzHnnzZc/Pmv5uKUNBu76v9glcYlXI0/img.jpg](https://blog.kakaocdn.net/dn/dIHQaC/btqLzHnnzZc/Pmv5uKUNBu76v9glcYlXI0/img.jpg)

이므로

![https://blog.kakaocdn.net/dn/vYsSF/btqLwKypfON/VYToOCz1KEQJDVkLfhSKP0/img.jpg](https://blog.kakaocdn.net/dn/vYsSF/btqLwKypfON/VYToOCz1KEQJDVkLfhSKP0/img.jpg)

가 된다.

![https://blog.kakaocdn.net/dn/o1DKE/btqLyKScNJe/0jIgWwywtOlcZV0dYkErmk/img.jpg](https://blog.kakaocdn.net/dn/o1DKE/btqLyKScNJe/0jIgWwywtOlcZV0dYkErmk/img.jpg)

와 같고

![https://blog.kakaocdn.net/dn/c1TLRQ/btqLvfy8mk4/6GQMJkDXKoaMjTQeKuRl81/img.jpg](https://blog.kakaocdn.net/dn/c1TLRQ/btqLvfy8mk4/6GQMJkDXKoaMjTQeKuRl81/img.jpg)

이다.

![https://blog.kakaocdn.net/dn/bf9Ew7/btqLzXwLPil/MI3Lk3dFvUIG5JILhH32Hk/img.jpg](https://blog.kakaocdn.net/dn/bf9Ew7/btqLzXwLPil/MI3Lk3dFvUIG5JILhH32Hk/img.jpg)

,

![https://blog.kakaocdn.net/dn/Tiov9/btqLwMbUbrj/eel1rkysda9kHxerafKVf0/img.jpg](https://blog.kakaocdn.net/dn/Tiov9/btqLwMbUbrj/eel1rkysda9kHxerafKVf0/img.jpg)

이므로

출력에는

![https://blog.kakaocdn.net/dn/bdXI3I/btqLve1idK2/Hj4Bsf2obwfV6yWJOzkeTK/img.jpg](https://blog.kakaocdn.net/dn/bdXI3I/btqLve1idK2/Hj4Bsf2obwfV6yWJOzkeTK/img.jpg)

만 영향을 끼친다는 것을 확인할 수 있다.

따라서

![https://blog.kakaocdn.net/dn/bKG4GA/btqLwfFmZXO/ZNoTTEPa1hlgnZSHb2xj60/img.jpg](https://blog.kakaocdn.net/dn/bKG4GA/btqLwfFmZXO/ZNoTTEPa1hlgnZSHb2xj60/img.jpg)

이므로

![https://blog.kakaocdn.net/dn/kODf7/btqLwKL1rZt/I106XckWgDxto65ImOysAK/img.jpg](https://blog.kakaocdn.net/dn/kODf7/btqLwKL1rZt/I106XckWgDxto65ImOysAK/img.jpg)

이다.

시간축으로 다시 변환을 해주면

![https://blog.kakaocdn.net/dn/ziJbs/btqLvflAUwX/9vZ5qQ0zUwl5VST5tsDolk/img.jpg](https://blog.kakaocdn.net/dn/ziJbs/btqLvflAUwX/9vZ5qQ0zUwl5VST5tsDolk/img.jpg)

가 된다.

![https://blog.kakaocdn.net/dn/zDf4A/btqLyKLqYEb/u3fukoGjZ4xarKKR305tM0/img.jpg](https://blog.kakaocdn.net/dn/zDf4A/btqLyKLqYEb/u3fukoGjZ4xarKKR305tM0/img.jpg)

의 그래프를 Matlab 에 도시화 하면 다음과 같다.

![https://blog.kakaocdn.net/dn/dE9JUf/btqLA2RTrO8/QdVIWpNGjvPLV9fPJ8q7tk/img.jpg](https://blog.kakaocdn.net/dn/dE9JUf/btqLA2RTrO8/QdVIWpNGjvPLV9fPJ8q7tk/img.jpg)

[Untitled](https://www.notion.so/8c3e7b677d984dedbff20a0e710d06d6)

![https://blog.kakaocdn.net/dn/KwqCO/btqLyLjh1Hu/jQQk9cZsagPQBnmjQanVN0/img.jpg](https://blog.kakaocdn.net/dn/KwqCO/btqLyLjh1Hu/jQQk9cZsagPQBnmjQanVN0/img.jpg)

의 그래프를 Matlab 에 도시화 하면 다음과 같다.

![https://blog.kakaocdn.net/dn/SRESU/btqLzYbmilG/XBGq3RizOqAX0kzjoEvYg1/img.jpg](https://blog.kakaocdn.net/dn/SRESU/btqLzYbmilG/XBGq3RizOqAX0kzjoEvYg1/img.jpg)

[Untitled](https://www.notion.so/ae0ed4e8b0844c208769909bfd060200)

![https://blog.kakaocdn.net/dn/dqm16P/btqLweNis8r/72sNKkrDmNSNooU5xDQwj0/img.jpg](https://blog.kakaocdn.net/dn/dqm16P/btqLweNis8r/72sNKkrDmNSNooU5xDQwj0/img.jpg)

![https://blog.kakaocdn.net/dn/7Jwo3/btqLzYh9PKY/hZ44rCsyEcfCVbIIkVnNpK/img.jpg](https://blog.kakaocdn.net/dn/7Jwo3/btqLzYh9PKY/hZ44rCsyEcfCVbIIkVnNpK/img.jpg)

의 주파수 응답을 Matlab 에 도시화 하면 다음과 같다.

[Untitled](https://www.notion.so/af5540ea8fea44beadd025cda2bc1c18)

[Untitled](https://www.notion.so/590b3b83558549c9959e259569e37daa)

![https://blog.kakaocdn.net/dn/ldE6C/btqLAzPV8p2/W7NxolYcb488MXFThod0t1/img.jpg](https://blog.kakaocdn.net/dn/ldE6C/btqLAzPV8p2/W7NxolYcb488MXFThod0t1/img.jpg)

필터의 주파수 응답을 Matlab 에 도시화 하면 다음과 같다.

![https://blog.kakaocdn.net/dn/lh8aq/btqLA4a6ZzT/MUeJpU2rvIWc5vklkJKzHk/img.jpg](https://blog.kakaocdn.net/dn/lh8aq/btqLA4a6ZzT/MUeJpU2rvIWc5vklkJKzHk/img.jpg)

필터의 임펄스 응답을 Matlab 에 도시화 하면 다음과 같다.

[Untitled](https://www.notion.so/397acf72440f4ed498018de9bf0425d3)

![https://blog.kakaocdn.net/dn/bc5c6F/btqLveNL7hD/SgOYJ507w6D5aJhblyQZe0/img.jpg](https://blog.kakaocdn.net/dn/bc5c6F/btqLveNL7hD/SgOYJ507w6D5aJhblyQZe0/img.jpg)

![https://blog.kakaocdn.net/dn/b0n2EW/btqLA3J2kG0/urlfwDpzOa9cyeEun4mgc1/img.jpg](https://blog.kakaocdn.net/dn/b0n2EW/btqLA3J2kG0/urlfwDpzOa9cyeEun4mgc1/img.jpg)

의 그래프를 Matlab 에 도시화 하면 다음과 같다.

[Untitled](https://www.notion.so/f45eb2bdf6674443b4570276298e17b6)

![https://blog.kakaocdn.net/dn/mg4ZE/btqLzGIMFFj/vfWoRXSQClGPatGdQFvxt1/img.jpg](https://blog.kakaocdn.net/dn/mg4ZE/btqLzGIMFFj/vfWoRXSQClGPatGdQFvxt1/img.jpg)

의 그래프를 Matlab 에 도시화 하면 다음과 같다

![https://blog.kakaocdn.net/dn/bD7ODY/btqLwd8FMWZ/GJ8h7iAgMKFKk3PlPwAEJk/img.jpg](https://blog.kakaocdn.net/dn/bD7ODY/btqLwd8FMWZ/GJ8h7iAgMKFKk3PlPwAEJk/img.jpg)

[Untitled](https://www.notion.so/b2a4e52abbc34e8580eea375c60c5618)
