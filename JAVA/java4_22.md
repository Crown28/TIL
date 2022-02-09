# 문제 4-22
기호 문자'*'를 나열해서 직각의 이등변 삼각형을 표시하는 프로그램을 작성하자. 직각의 위치가 왼쪽 아래, 왼쪽 위, 오른쪽 아래, 오른쪽 위에 표시하는 프로그램을 각각 작성할 것.

## 1.  왼쪽 아래가 직각인 이등변 삼각형
```
import java.util.Scanner;

class LB{
  public static void main (String [] args){
    Scanner scanner = new Scanner(System.in);

    System.out.println("왼쪽 아래가 직각인 별찍기");
    System.out.println("단수는? :");
    int n = scanner.nextInt();

    for(int i=1; i<=n; i++){
      for(int j=1; j<=i; j++)
        System.out.print('*');
      System.out.println();
    }
  }
}
```

## 실행 결과
> 왼쪽 아래가 직각인 이등변 삼각형을 표시합니다.
> <br>단수는? :5
> <br>*
> <br>**
> <br>***
> <br>****
> <br>*****

---
<br>

## 2.  왼쪽 위가 직각인 이등변 삼각형
```
import java.util.Scanner;

class LU{
  public static void main (String [] args){
    Scanner scanner = new Scanner(System.in);

    System.out.println("왼쪽 위가 직각인 별찍기");
    System.out.println("단수는? :");
    int n = scanner.nextInt();

    for(int i=1; i<=n; i++){
      for(int j=1; j<=n-i+1; j++)
        System.out.print('*');
      System.out.println();
    }
  }
}
```

## 실행 결과
> 왼쪽 아래가 직각인 이등변 삼각형을 표시합니다.
> <br>단수는? :5
> <br>*****
> <br>****
> <br>***
> <br>**
> <br>*

---

## 3.  오른쪽 아래가 직각인 이등변 삼각형
```
import java.util.Scanner;

class RB{
  public static void main (String [] args){
    Scanner scanner = new Scanner(System.in);

    System.out.println("오른쪽 아래가 직각인 별찍기");
    System.out.println("단수는? :");
    int n = scanner.nextInt();

    for(int i=1; i<=n; i++){
      for(int j=1; j<=n-1; j++)
        System.out.print('');
      for(int j=1; j<=i; j++)
        System.out.print('*');
      System.out.println();
    }
  }
}
```

## 실행 결과
> 오른쪽 아래가 직각인 이등변 삼각형을 표시합니다.
> <br>단수는? :5
> <br>&nbsp;&nbsp;&nbsp;&nbsp;*
> <br>&nbsp;&nbsp;&nbsp;**
> <br>&nbsp;&nbsp;***
> <br>&nbsp;****
> <br>*****

---

## 3.  오른쪽 위가 직각인 이등변 삼각형
```
import java.util.Scanner;

class RU{
  public static void main (String [] args){
    Scanner scanner = new Scanner(System.in);

    System.out.println("오른쪽 위가 직각인 별찍기");
    System.out.println("단수는? :");
    int n = scanner.nextInt();

    for(int i=1; i<=n; i++){
      for(int j=1; j<=i-1; j++)
        System.out.print('');
      for(int j=1; j<=n-i+1; j++)
        System.out.print('*');
      System.out.println();
    }
  }
}
```

## 실행 결과
> 오른쪽 아래가 직각인 이등변 삼각형을 표시합니다.
> <br>단수는? :5
> <br>*****
> <br>&nbsp;****
> <br>&nbsp;&nbsp;***
> <br>&nbsp;&nbsp;&nbsp;**
> <br>&nbsp;&nbsp;&nbsp;&nbsp;*

---

*출처 : 알쏭달쏭 자바 200제*