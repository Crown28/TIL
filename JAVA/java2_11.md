# 문제 2-11
###다음과 같은 프로그램을 작성하자
* 한 자리 양의 정숫값을 랜덤으로 생성해서 표시
* 한 자리 음의 정숫값을 랜덤으로 생성해서 표시
* 두 자리 양의 정숫값을 랜덤으로 생성해서 표시

```
import java.util.Random;

class RandomInteger{
  public static void main(String[] args){
    Random rand = new Random();

    int n1 = 1 + rand.nextInt(9);
    int n2 = -1 - rand.nextInt(9);
    int n3 = 10 + rand.nextInt(90);

    System.out.println("3개의 난수를 생성했습니다.");
    System.out.println("한 자리 양의 정수:" + n1);
    System.out.println("한 자리 음의 정수:" + n2);
    System.out.println("두 자리 양의 정수:" + n3);
  }
}
```

### 난수 생성
랜덤으로 생성되는 값을 난수라고 한다. `rand.nextInt(n)`은 0이상 n미만의 랜덤한 정숫값을 만든다. `rand.nextInt(9)`의 값은 0~8이 되며, `rand.nextInt(90)`의 값은 0~89가 되므로 각 변수는 다음과 같이 초기화된다.
* 변수 n1 : 0~8에 1을 더한 1~9
* 변수 n2 : 0~8에 부호를 반대로 한 0~-8에 -1을 더한 -1~-9
* 변수 n3 : 0~89에 10을 더한 10~99

*출처 : 알쏭달쏭 자바 200제*