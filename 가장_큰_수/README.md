음..... 사실 그렇게 어려운 문제는 아닙니다. 하지만 이 문제가 그렇게나 어려운 이유는 시간초과때문이겠죠.

itertools의 퍼뮤테이션을 사용한 최댓값 산정하기도 하나의 방법일것이구요.
이전에 어떤 문제를 풀다가 비슷한 문제를 맞이한 적이 있더라면 str의 정렬에 대한 특성을 떠올려 직접 정렬해보려고 하다가도 한두개의 예외에서 문제를 맞이하게 되것입니다.

이렇게 시간이 아슬아슬하게 설계된 문제에서는 애써 힘쓰지 말고 이번 문제를 교훈 삼았다고 생각하고 너무 고생하진 말았으면 좋겠습니다.
위에서 말했던 str sorting 방식으로 접근했을때의 예외는 이런식에서 말생합니다.

우리는 사실 "앞자리가 큰수로 왔으면 좋겠다 !" 라는 생각에 문자열을 솔팅하고 그것을 뒤집을것입니다.
왜냐면 str인 숫자 자료형은 사전 정렬을 하면 1~9 순으로 그것을 자리수라고 계산하지 않고 인덱스로 산정하여 1111111이 234보다 앞에 올 수 있게 되는것입니다.
하지만 이렇게 하면 문제가 하나 발생하는데, 글자의 제한이 3자리라고 하였으니 22 와 221이 있으면 정렬시에 그대로 22다음 221가 올 것입니다.
하지만 이것을 우리는 가장 크게 만드는 조합으로 만들기 위해서 배열의 순서를 뒤집는데, 이 때 221와 22가 되고, 이 순대로 조합을 한다면 22122, 
오히려 22221보다 작게 됩니다. 이것은 하나를 크게 간과했기 때문인데, str솔팅의 경우 인덱스가 차이가 나고 , 작은 인덱스 기준으로 갚이 같다면 인덱스가 긴 쪽이
한 순위 밀린다는 것입니다. 

해당 부분을 제곱을 통해 해결해나갈 수 있습니다. 참고로 문자열을 제곱하면 문자열문자열 이 됩니다.

그렇기에 이를 넉넉하게 4제곱하며 자리수에서 생길 수 있는 오차를 없앤 후 정렬을 하는것입니다. 

22 와 221은  221이 뒤로 가야함이 분명하지만, 네제곱 한 22222222와 221221221221 은 자리수 차이는 더욱 극명하게 갈리지만 인덱스가 작은 요소를 
기반으로 대소관계를 비교하더라도 중간에 들어있는 1이 발목을 잡게 되어 우리가 원하는대로 정렬이 가능하게 되는것입니다.

이후 아이디어는 알아서 구현할 수 있으리라 믿습니다.
