# 문제 6-7
시험 점수의 합계, 평균, 최고점, 최저점을 구하는 프로그램을 작성하자. 사람 수와 점수는 키보드를 통해 입력 받을 것.

```
import java.util.Scanner;

class PointSumAve{
  public static void main(String[] args){
    Scanner stdIn = new Scanner(System.in);

    System.out.print("사람 수:");
    int n = stdIn.nextInt();
    int[] points = new int[n];

    System.out.println("점수를 입력하세요.");
    int sum = 0;
    for(int i =0; i<n; i++){
      System.out.print((i+1)+"번의 점수:");
      points[i] = stdIn.nextInt();
      sum += points[i];
    }

    int max = points[0];
    int min = points[0];
    for(int i=1; i<n; i++){
      if(points[i]>max)
        max = points[i];
      if(points[i]<min)
        min = points[i];
    }

    System.out.println("합계는 "+sum+"점입니다.");
    System.out.println("평균은 "+(double)sum/n+"점입니다.");
    System.out.println("최고점은 " + max + "점입니다.");
    System.out.println("최고점은 " + min + "점입니다.");
  }
}
```
