사실 몹시 쉬운편에 속하는 문제이긴 합니다.
하지만 최근들어 재귀함수를 이용하는 문제를 잘 출제하는 시기가 아니라서, 재귀를 통해 푸는것이 일반적인 문제였기 때문에, 
많이 당황했을 수도 있다고 생각이 듭니다. <br><br><br>
재귀함수를 써야 하는 순간은 이러합니다.
<br>
1. 반복적인 작업은 필요하지만, 작업물을 계속 넘겨줘야 할 때.
2. 반복을 하면서 세어야 할 수치들이나, 변화값을을 계속 알아내야 할 때.

다음과 같은 조건들을 이번 문제는 모두 충족하고 있습니다.
1번 조건의 경우 , 말로만 들을 경우 "내가 이런 상황을 겪어 봤나 ?" 하는 생각이 들 수도 있는데, 지금 해당 문제를 풀면서 이런 니즈를 겪어
본 적이 있는지 확인 해보시길 바랍니다.

1. 0 지우기. 지우고 남은 1의 개수를 이진수로 변환하기. 무한 반복하기.
2. 반복을 몇 번 했는지, 0은 몇번 없앴는지 기록을 해야 문제를 제대로 풀 수 있음을 깨달기
3. 반복문으로 작성하려 했으나 Iterator로 걸어놓은 s가 계속 길이가 변화하여 오류가 남.

그럼 특정 반복문에서 Iterator가 유동적으로 변화해야 하는데, 이런 부분을 챙겨가기 위해선 재귀함수의 사용이 절실합니다.
함수를 작성하고, 그 함수의 끝에 다시 자기 자신을 호출하면서 뺑뻉 도는 형태인데, 함수는 매개변수, Parameter가 
존재한다는 사실을 배웠었습니다. Parameter는 이 재귀함수 안에서만큼은 엄청난 존재감을 자랑합니다.
마치 이어달리기에서의 바통이랄까요, 그 바통이 한바퀴 돌때마다 길이가 줄어든다는 상상력으로 연상하시면 이번 문제를 어떻게 
풀어나가야 할 지 느낌이 오실겁니다.<br>
고로 함수를 작성하고, 다시 호출하는 그 굴래 속에서 parameter는 꼭 똑같이 받아줘야 합니다.

Parameter의 경우는 내가 세어야 할 것, 넘겨줘야 할 것들이 있겠네요.


반복횟수, 2진수로 변환한 숫자, 없앤 0의 갯수 가 있겠네요.

참고로 쌈빡하게 변수 두개로 저글링 하면서 반복문 하나로 풀 수 있습니다. 예제 코드는 올려 놓을게요 !
재귀로 구현하고 싶은 어떠한 방법들은 대부분 While문으로 해결 할 수 있다는 점 기억 해두세요.
그럼 즐코 !



