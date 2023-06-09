문제가 대충 길쭉한데 핵심만 읽으면 마음이 편합니다.

규칙이 3개 있는데

1. 숫자는 시작으로 나올수도 ~ 안나올수도 있다. 하지만 그 이후는 절대 안나온다.
2. 숫자로만 이루어진 단어는 없다 == 한글자짜리가 있을 수 있지만 그럴땐 문자형태다.
3. 공백은 연속으로 나올 수 있다 == 뭐가 되었던 공백하나로 함축하여라 

조건문을 얼마나 깔끔하게 잘 짤 수 있느냐만을 물어보고 있습니다. 
문자열을 다루는 문제처럼 위장하고 있지만, 사실상 Python의 Split기능은
생각보다 영특하기 때문에 문자열에서는 크게 집중 할 포인트가 없습니다.

풀이는 이런식입니다.

1. list, map, split 국민 조합으로 전처리 후 배열으로 포팅할 것.
2. 규칙에서 중요도를 먼저 정하고 도식화 할 것. 해당 상황에선 첫글자에서 변별력이
   생기고 있기에 규칙 1번에 먼저 기준할 것. 해당 상황에선 첫 글자가 문자인지, 숫자인지 구별하는
   여러 방법이 있음. (1.Type함수로 구별, 2.Try except 문법을 통하여 int를 str으로 형변환 시켜보가, 3.isalpha())
3. 이후에 여러 규칙에 따라 조건문으로 처리할 것. split으로 공백이 없어진 문자에 대하여 앞글자 upper, 이후는 모두 lower.
   배열처리할때 멍청하게 반복하지 말고 slicing 할 것. [1:]
4. 이후 배열을 문자열로 조합하는 과정을 join으로 깔쌈하게 끝낼 것.

여러 포인트들을 참조 해서 쌈빡하게 코딩하시길

해당 문제에서 볼 수 있는 역량은 이러합니다. 
1. 특정 Data가 어떤 type인지에 따른 변별을 어떤 형식으로 깔끔하게 해낼 수 있는가 ?
2. 문자열을 어떤형식으로 접근해서 처리하고, 조합할 수 있는가 ? 자료형간의 경계를 유연하게 넘기고 있는가 ?

2가지를 어필하는 개발자라고 본인을 생각하면서 코드를 짜보면 좋겠습니다.
