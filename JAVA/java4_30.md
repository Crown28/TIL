# 문제 4-30

0~99사이의 정수를 맞추는 게임을 만들어보자. 제한 횟수 내에 맞추지 못한 경우에는 정답을 표시하고 게임을 종료할 것.

```
import java.util.Random;
import java.util.Scanner;

class FindNumber {
  public static void main(String[] args){
    Random rand = new Random();
    Scanner scanner = new Scanner(System.in);

    final int MAX_NO = 6; // 최대 입력 횟수
    int leftNo = MAX_NO; // 남은 횟수
    int no = rand.nextInt(100); // 맞춰야 하는 숫자 0~99

    System.out.println("숫자 맞추기 게임 시작!");
    System.out.println("0~99사이의 숫자 맞춰봐.");

    int x;
    do{
      System.out.println("남은 횟수 "+(leftNo--)+"회, 어떤 숫자일까?:");
      x = scanner.nextInt();

      if(x>no)
        System.out.println("더 작은 숫자입니다.");
      else if(x<no)
        System.out.println("더 큰 숫자입니다.");
    }while(x!=no&&leftNo>0);

    if(x==no)
      System.out.print((MAX_NO - leftNo)+"회 만에 맞추었습니다.");
    else
      System.out.print("아쉽네요 정답은"+no+"입니다.");

  }
}
```

## 숫자 맞추기 게임
플레이어가 입력할 수 있는 최대 횟수는 `final` 변수인 MAX_NO를 이용해 6회로 지정한다. 변수 leftNo는 남은 횟수를 저장하며 초깃값은 MAX_NO와 동일한 6이다. 플레이어가 값을 입력할 때마다 6,5,4..로 감소하며 0이 되면 게임을 종료한다.
<br> do 문의 조건식인 x!=no와 leftNo>0은 논리곱 연산자인 &&로 연결된다. 따라서 숫자를 맞춘 경우뿐만 아니라 leftNo가 0이 된 경우에도 반복이 종료된다. 몇 번만에 맞추었는지는 MAX_NO에서 leftNO를 빼면 알 수 있다. 평균적으로 가장 빨리 맞추는 방법이 있다. 처음에 50을 입력하고 그것보다 큰지, 작은지에 따라서 75 또는 25를 입력하는 방법이다. 즉, 반씩 범위를 줄여나가면 된다.

*출처 알쏭달쏭 자바 200제*