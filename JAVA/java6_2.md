# 문제 6-2
요소 개수가 5개인 int형 순서대로 5,4,3,2,1을 대입하는 프로그램을 작성하자.
```
class IntArrayFor{
  public static void main(String[] args){
    int[]a = new int[5];

    for (int i = 0; i<a.length; i++)
      a[i] = 5-i;

    for (int i = 0; i<a.length; i++)
      System.out.println("a["+i+"]=" + a[i]);
  }
}
```

### 실행 결과
```
a[0]=5
a[1]=4
a[2]=3
a[3]=2
a[4]=1
```

## 요소 수 가져오기
IntArrayFor 프로그램에서 사용하는 int형 배열은 각 요소에 값을 대입한 후 각 요소를 표시한다. 요소에 값을 대입하는 것이 첫 번째 for문이고 요솟값을 표시하는 것이 두 번째 for문이다. 제어식 부분(a.length)은 다음과 같은 식을 사용한다.
> 배열변수명.length

위 식은 배열의 요소 수를 가져오는 식이다. 요소 수는 길이(length)라고도 한다. 여기서는 a.length를 평가한 값이 5이다. 

*출처 알쏭달쏭 자바 200제*