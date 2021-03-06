# 문제 4-2
3자리의 양의 정숫값을 읽는 프로그램을 작성하라. (입력한 값이 3자리 양의 정숫값이 아니면 다시 입력하게 할 것)

```
import java.util.Scanner

class ThreeDigits{
  public static void main(String[] args){
    Scanner scanner = new Scanner(System.in);
    int x;
    do{
      System.out.print("세 자리의 정숫값:");
      x = scanner.nextInt();
    }while(x<100 || x>999);

    System.out.print("입력한 값은 "+"입니다.");
  }
}
```
## 실행 예
```
세 자리의 정숫값:59
세 자리의 정숫값:1044
세 자리의 정숫값:530
입력한 값은 527입니다.
```
---
## 드모르간의 법칙
do문의 조건식인 (x < 100 || x>999)에 주목하자. 변수 x의 값이 세 자리의 양의 정수가 아닌 경우는, 이 식을 평가한 값이 true가 된다. 따라서 x가 **3자리의 양의 정수가 아닌 경우** 루프 바디가 반복 실행되며 "세 자리의 양의 정숫값:"을 표시해서 다시 입력해야 한다.

do문의 조건식을 논리 부정 연산자를 사용해서 작성하면 다음과 같이 된다.
> !(x >= 100 && x <= 999>)

'각 조건을 부정한 후, 논리합 및 논리곱을 서로 바꾼 식'의 부정은 원래 조건과 같다. 이것을 드모르간의 법칙(De Morgan's laws)이라고 한다. 이 규칙을 식으로 나타내면 다음과 같다.
* x&&y 와!(!x||!y)는 같다
* x||y 와!(!x&&!y)는 같다 

*출처 : 알쏭달쏭 자바 200제*